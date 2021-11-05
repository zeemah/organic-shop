<template>
  <div class="min-h-screen sm:flex sm:flex-row  mx-0 justify-center bg-gray-900">
    <div class="logo-container justify-center mt-52">
      <img src="~/assets/img/organic.png" width="200" class="justify-center"/>
    </div>
      <div class="flex justify-center self-center  z-10">
        <div class="p-12 bg-white mx-auto rounded-2xl w-100 mt-24">
            <div class="mb-4">
              <h3 class="font-semibold text-2xl text-gray-800">Sign In </h3>
            </div>
            <div class="space-y-5">
                        <div class="space-y-2">
                              <label class="text-sm font-medium text-gray-700 tracking-wide">Email*</label>
              <input class=" w-full text-base px-4 py-2 border  border-gray-300 rounded-lg focus:outline-none focus:border-yellow--400" type="text" placeholder="user@mail.com">
              </div>
                          <div class="space-y-2">
              <label class="mb-5 text-sm font-medium text-gray-700 tracking-wide">
                Password*
              </label>
              <input class="w-full content-center text-base px-4 py-2 border  border-gray-300 rounded-lg focus:outline-none focus:border-yellow-400" type="password" placeholder="Enter your password">
            </div>
              <div class="flex items-center justify-between">
              <div class="flex items-center">
                <input id="remember_me" name="remember_me" type="checkbox" class="h-4 w-4 bg-blue-500 focus:ring-blue-400 border-gray-300 rounded">
                <label for="remember_me" class="ml-2 block text-sm text-gray-800">
                  Remember me
                </label>
              </div>
              <div class="text-sm">
                <NuxtLink to="/auth/reset" class="text-yellow-400 hover:text-yellow-500">
                  Forgot your password?
                </NuxtLink>
              </div>
            </div>
            <div>
              <button type="submit" class="w-full flex justify-center bg-yellow-500  hover:bg-yellow-400 text-gray-100 p-3 rounded-full tracking-wide font-semibold  shadow-lg cursor-pointer transition ease-in duration-500">
                Sign in
              </button>
            </div>
            </div>
            <div class="pt-5 text-center text-gray-400 text-xs">
              <span>
                Copyright Ⓒ {{ year }}
                <a href="#" rel="" title="organic-shop" class="text-yellow-400 hover:text-yellow-500 ">Organic Shop</a>
                </span>
            </div>
        </div>
      </div>
  </div>
</template>


<script>
  export default {
   data(){
      return {
          year: new Date().getFullYear()
      }
    }
  }
</script>
