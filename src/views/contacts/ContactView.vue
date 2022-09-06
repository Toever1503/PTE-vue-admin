<template>
  <div id="contact">
    <div class="bg-[#1976d2] p-[100px] text-3xl text-center">
      <h1 class="text-white font-bold">
        Liên hệ tư vấn miễn phí các khóa học của chúng tôi
      </h1>
    </div>

    <div class="max-w-[600px] m-auto">
      <div class="text-center m-auto mt-[50px]">
        <h2 class="text-3xl font-bold">Đăng ký tư vấn và hỗ trợ </h2>
        <p class="text-xl">
          Vui lòng điền các thông tin liên hệ, HOCPTE sẽ liên hệ và giải đáp các thắc mắc của bạn trong thời gian sớm
          nhất.
        </p>
      </div>

      <div class="form_contact pt-[50px]">
        <a-form
            :model="formState"
            name="basic"
            :wrapper-col="{ span: 16 }"
            autocomplete="off"
        >
          <a-form-item
              name="username"
              :rules="[{ required: true, message: 'Vui lòng điền họ tên!' }]"
          >
            <a-input v-model:value="formState.username" placeholder="Họ và Tên"/>
          </a-form-item>

          <a-form-item
              name="password"
              :rules="[{ required: true, message: 'Vui lòng điền số điện thoại!' }]"
          >
            <a-input v-model:value="formState.password" placeholder="Số điện thoại"/>
          </a-form-item>

          <a-form-item
              name="username"
              :rules="[{ required: true, message: 'Vui lòng điền địa chỉ email!' }]"
          >
            <a-input v-model:value="formState.username" placeholder="Địa chỉ email"/>
          </a-form-item>

          <a-form-item
              name="password"
              :rules="[{ required: true, message: 'Vui lòng không để trống!' }]"
          >
            <a-input v-model:value="formState.password" placeholder="Bạn muốn tư vấn thông tin như thế nào?"/>
          </a-form-item>

          <a-form-item class="text-center">
            <a-button type="primary" html-type="submit">Gửi thông tin</a-button>
          </a-form-item>
        </a-form>
      </div>
    </div>

    <div class="more_info w-full bg-[#f3f9ff] py-[40px] px-[50px]"
         style="border-top: 1px solid #e1f5fe; border-bottom: 1px solid #e1f5fe">

      <div class="p-[20px] text-2xl text-center">
        <h1 class="font-bold">
          Liên hệ với HOCPTE
        </h1>
        <div class="inline-block w-[100px] rounded h-[5px] bg-[#00b0ff]"></div>
      </div>
      <div class="max-w-[1000px] m-auto flex">
        <ul class="w-1/2 list_content">
          <li class="relative pl-[20px]">
            <h2 class="text-sm font-bold inline-block">Địa chỉ: </h2>
            <p class="inline-block pl-[5px]">
              123 Trần Hưng Đạo, Phường 5, Quận 5, TP. Hồ Chí Minh
            </p>
          </li>

          <li class="relative pl-[20px] my-[10px]">
            <h2 class="text-sm font-bold inline-block">Điện thoại:</h2>
            <p class="inline-block pl-[5px]">
              0123456789
            </p>
          </li>

          <li class="relative pl-[20px]">
            <h2 class="text-sm font-bold inline-block">Email:</h2>
            <p class="inline-block pl-[5px]">
              0123456789
            </p>
          </li>
        </ul>

        <div>
          <h2 class="text-xl font-bold text-center">Kết nối với HOCPTE trên mạng xã hội</h2>
          <ul class="flex gap-[10px] m-auto w-fit">
            <li>
              <google-outlined/>
            </li>
            <li>
              <twitter-outlined/>
            </li>
            <li>
              <youtube-outlined/>
            </li>
            <li>
              <instagram-outlined/>
            </li>
            <li>
              <facebook-outlined/>
            </li>
          </ul>
        </div>

      </div>
    </div>

  </div>

</template>

<script setup>
import {reactive} from "vue";
import {
  GoogleOutlined,
  TwitterOutlined,
  YoutubeOutlined,
  InstagramOutlined,
  FacebookOutlined
} from "@ant-design/icons-vue";

const formState = reactive({
  username: '',
  password: '',
  remember: true,
});


</script>

<style>
#contact .form_contact .ant-col.ant-col-16.ant-form-item-control {
  margin: auto;
}

#contact .list_content li:before {
  content: "";
  width: 8px;
  height: 8px;
  border-radius: 50%;
  position: absolute;
  top: 8px;
  left: 4px;
  background: #00b0ff;
}
</style>