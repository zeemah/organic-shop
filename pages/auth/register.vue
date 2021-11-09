<template>
   <div class="font-sans min-h-screen antialiased bg-gray-900 pt-24 pb-5">
    <div class="flex flex-col justify-center sm:w-96 sm:m-auto mx-5 mb-5 space-y-8">
      <!-- <h1 class="font-bold text-center text-4xl text-yellow-500">Your<span class="text-blue-500">App</span></h1> -->
      <img src="~/assets/img/organic.png" width="200" class="justify-center lg:pt-56 lg:ml-24"/>
      <form action="#">
        <div class="flex flex-col bg-white p-10 rounded-lg shadow space-y-6">
          <h1 class="font-bold text-xl text-center">Create your account</h1>
          
          <div class="flex flex-col space-y-1">
             <label class=" text-sm font-medium text-gray-700 tracking-wide">
              Name*
            </label>
            <input type="text" name="name" id="name" class="border-2 rounded px-3 py-2 w-full focus:outline-none focus:border-yellow-400 focus:shadow" placeholder="Jane Doe" required />
          </div>

          <div class="flex flex-col space-y-1">
             <label class=" text-sm font-medium text-gray-700 tracking-wide">
              Email*
            </label>
            <input type="text" name="username" id="username" class="border-2 rounded px-3 py-2 w-full focus:outline-none focus:border-yellow-400 focus:shadow" placeholder="Jane@mail.com" required />
          </div>

          <div class="flex flex-col space-y-1">
            <label class="text-sm font-medium text-gray-700 tracking-wide">
             Password*
            </label>
            <input type="password" name="password" id="password" class="border-2 rounded px-3 py-2 w-full focus:outline-none focus:border-yellow-400 focus:shadow" placeholder="Password" required/>
          </div> 
          <div class="flex flex-col-reverse sm:flex-row sm:justify-between items-center">
            <NuxtLink to="/auth/login" class="inline-block text-yellow-500 hover:text-yellow-800">Back to Login</NuxtLink>
            <button type="submit" class="bg-yellow-500 text-white font-bold px-5 py-2 rounded focus:outline-none shadow hover:bg-yellow-600 transition-colors">Create account</button>
          </div>
        </div>
      </form>
      <div class="flex justify-center text-gray-500 text-sm">
        <p>&copy;{{ year }}. All right reserved.</p>
      </div>
    </div>
  </div>
</template>


<script>
  export default {
   data(){
      return {
          year: new Date().getFullYear(),
          
      }
    }
  }
</script>
