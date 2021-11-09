<template>
  <div class="bg-gray-900">
   <NavHeader/>
    <main class="my-8">
      <div class="container mx-auto px-6">
        <div class="container">
        <div class="max-w-md w-full bg-gray-800 shadow-lg rounded-xl p-6">
        <div class="flex flex-col ">
          <div class="">
            <div class="relative h-62 w-full mb-3">
              <div class="absolute flex flex-col top-0 right-0 p-3">
                <button class="transition ease-in duration-300 bg-gray-800  hover:text-purple-500 shadow hover:shadow-md text-gray-500 rounded-full w-8 h-8 text-center p-1"><svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                  </svg></button>
              </div>
              <img src="https://media.istockphoto.com/photos/love-taking-care-of-my-skin-picture-id1280517978?b=1&k=20&m=1280517978&s=170667a&w=0&h=WONhaHZ7tHzRCdob6V2Sn3-cYjRWyExWq7mAAwzZIOw=" alt="Just a flower" class=" w-full   object-fill  rounded-2xl">
            </div>
            <div class="flex-auto justify-evenly">
              <div class="flex flex-wrap ">
                <div class="w-full flex-none text-sm flex items-center text-gray-600">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-red-500 mr-1" viewBox="0 0 20 20" fill="currentColor">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                  </svg>
                  <span class="text-gray-400 whitespace-nowrap mr-3">4.60</span><span class="mr-2 text-gray-400">India</span>
                </div>
                <div class="flex items-center w-full justify-between min-w-0 ">
                  <h2 class="text-lg mr-auto cursor-pointer text-gray-200 hover:text-purple-500 truncate ">Lorem ipsum
                    is placeholder text commonly used in the graphic</h2>
                  <div class="flex items-center bg-green-400 text-white text-xs px-2 py-1 ml-3 rounded-lg">
                    INSTOCK</div>
                </div>
              </div>
              <div class="text-xl text-white font-semibold mt-1">$240.00</div>
              
              
                      
              <div class="flex items-center mt-1">
                <label class="text-gray-700 text-sm mr-2" for="count">Count:</label>
                  <button class="text-gray-500 focus:outline-none focus:text-gray-600">
                      <svg class="h-5 w-5" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                  </button>
                  <span class="text-gray-700 text-lg mx-2">20</span>
                  <button class="text-gray-500 focus:outline-none focus:text-gray-600">
                      <svg class="h-5 w-5" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M15 12H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                  </button>
              </div>
              <div class="flex space-x-2 text-sm font-medium justify-start">
                <button class="transition ease-in duration-300 inline-flex items-center text-sm font-medium mb-2 md:mb-0 bg-purple-500 px-5 py-2 hover:shadow-lg tracking-wider text-white rounded-full hover:bg-purple-600 ">
                  <span>Add Cart</span>
                </button>
                <button class="transition ease-in duration-300 bg-gray-700 hover:bg-gray-800 border hover:border-gray-500 border-gray-700 hover:text-white  hover:shadow-lg text-gray-400 rounded-full w-9 h-9 text-center p-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
         </div>
         
          <div class="mt-16">
              <h3 class="text-gray-600 text-2xl font-medium">More Products</h3>
              <div class="grid gap-6 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 mt-6">
                  <div class="w-full max-w-sm mx-auto rounded-md shadow-md overflow-hidden">
                      <div class="flex items-end justify-end h-56 w-full bg-cover" style="background-image: url('https://images.unsplash.com/photo-1563170351-be82bc888aa4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=376&q=80')">
                          <button class="p-2 rounded-full bg-blue-600 text-white mx-5 -mb-4 hover:bg-blue-500 focus:outline-none focus:bg-blue-500">
                              <svg class="h-5 w-5" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                          </button>
                      </div>
                      <div class="px-5 py-3">
                          <h3 class="text-gray-700 uppercase">Chanel</h3>
                          <span class="text-gray-500 mt-2">$12</span>
                      </div>
                  </div>
                  <div class="w-full max-w-sm mx-auto rounded-md shadow-md overflow-hidden">
                      <div class="flex items-end justify-end h-56 w-full bg-cover" style="background-image: url('https://images.unsplash.com/photo-1544441893-675973e31985?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1500&q=80')">
                          <button class="p-2 rounded-full bg-blue-600 text-white mx-5 -mb-4 hover:bg-blue-500 focus:outline-none focus:bg-blue-500">
                              <svg class="h-5 w-5" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                          </button>
                      </div>
                      <div class="px-5 py-3">
                          <h3 class="text-gray-700 uppercase">Man Mix</h3>
                          <span class="text-gray-500 mt-2">$12</span>
                      </div>
                  </div>
                  <div class="w-full max-w-sm mx-auto rounded-md shadow-md overflow-hidden">
                      <div class="flex items-end justify-end h-56 w-full bg-cover" style="background-image: url('https://images.unsplash.com/photo-1532667449560-72a95c8d381b?ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80')">
                          <button class="p-2 rounded-full bg-blue-600 text-white mx-5 -mb-4 hover:bg-blue-500 focus:outline-none focus:bg-blue-500">
                              <svg class="h-5 w-5" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                          </button>
                      </div>
                      <div class="px-5 py-3">
                          <h3 class="text-gray-700 uppercase">Classic watch</h3>
                          <span class="text-gray-500 mt-2">$12</span>
                      </div>
                  </div>
                  <div class="w-full max-w-sm mx-auto rounded-md shadow-md overflow-hidden">
                      <div class="flex items-end justify-end h-56 w-full bg-cover" style="background-image: url('https://images.unsplash.com/photo-1590664863685-a99ef05e9f61?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=345&q=80')">
                          <button class="p-2 rounded-full bg-blue-600 text-white mx-5 -mb-4 hover:bg-blue-500 focus:outline-none focus:bg-blue-500">
                              <svg class="h-5 w-5" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
                          </button>
                      </div>
                      <div class="px-5 py-3">
                          <h3 class="text-gray-700 uppercase">woman mix</h3>
                          <span class="text-gray-500 mt-2">$12</span>
                      </div>
                  </div>
              </div>
          </div>
      </div>
    </main>
    <NavFooter/>
</div>
</template>


<script>
  export default {
   data(){
      return {
          // year: new Date().getFullYear()
      }
    }
  }
</script>
