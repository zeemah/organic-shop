<template>
    <div x-data="setup()" x-init="$refs.loading.classList.add('hidden'); setColors(color);" :class="{ 'dark': isDark}" class="">
      <div class="flex h-screen antialiased text-gray-900 bg-gray-100 dark:bg-dark dark:text-light">
        <!-- Loading screen -->
        <div x-ref="loading" class="fixed inset-0 z-50 flex items-center justify-center text-2xl font-semibold text-white bg-primary-darker hidden">
          Loading.....
        </div>

        <SideBar/>

        <div class="flex-1 h-full overflow-x-hidden overflow-y-auto">
          <!-- Navbar -->
         <DashHeader/>
          <!-- Main content -->
           <div class="flex items-center justify-between px-10 py-4 border-b lg:py-6 dark:border-primary-darker">
              <h1 class="text-2xl font-semibold">Sales</h1>

              <div class="flex items-center select-none">
					<span class="hover:text-pink-500 cursor-pointer mr-3">

						<svg viewBox="0 0 512 512" class="h-5 w-5 fill-current">
							<path
								d="M505 442.7L405.3
								343c-4.5-4.5-10.6-7-17-7H372c27.6-35.3 44-79.7
								44-128C416 93.1 322.9 0 208 0S0 93.1 0 208s93.1
								208 208 208c48.3 0 92.7-16.4 128-44v16.3c0 6.4
								2.5 12.5 7 17l99.7 99.7c9.4 9.4 24.6 9.4 33.9
								0l28.3-28.3c9.4-9.4 9.4-24.6.1-34zM208 336c-70.7
								0-128-57.2-128-128 0-70.7 57.2-128 128-128 70.7 0
								128 57.2 128 128 0 70.7-57.2 128-128 128z"></path>
						</svg>
					</span>

					<input
						class="bg-transparent focus:outline-none"
						placeholder="Search Sales..." />

				</div>

				

				<div class="flex items-center select-none">
                    <button
					class="ml-3 bg-gray-400 dark:bg-gray-600
						dark:text-gray-400 rounded-full p-2 focus:outline-none
						hover:text-yellow-500 hover:bg-yellow-700 transition
						duration-500 ease-in-out">
					<svg class="h-5 w-5 fill-current mr-1" viewBox="0 0 24 24">
						<path
							d="M12 1L8 5h3v9h2V5h3m2 18H6a2 2 0 01-2-2V9a2 2 0
							012-2h3v2H6v12h12V9h-3V7h3a2 2 0 012 2v12a2 2 0 01-2
							2z"></path>
					</svg>
					<!-- <span>Export</span> -->
				</button>
					<!-- <span>Filter</span> -->
					<button
						class="ml-3 bg-gray-400 dark:bg-gray-600
						dark:text-gray-400 rounded-full p-2 focus:outline-none
						hover:text-pink-500 hover:bg-pink-300 transition
						duration-500 ease-in-out">
						<svg class="h-5 w-5 fill-current" viewBox="0 0 24 24">
							<path
								d="M14 12v7.88c.04.3-.06.62-.29.83a.996.996 0
								01-1.41 0l-2.01-2.01a.989.989 0
								01-.29-.83V12h-.03L4.21 4.62a1 1 0
								01.17-1.4c.19-.14.4-.22.62-.22h14c.22 0
								.43.08.62.22a1 1 0 01.17 1.4L14.03 12H14z"></path>
						</svg>
					</button>
					<button
						class="ml-2 bg-gray-400 dark:bg-gray-600
						dark:text-gray-400 rounded-full p-2 focus:outline-none
						hover:text-pink-500 hover:bg-pink-300 transition
						duration-500 ease-in-out">
						<svg class="h-5 w-5 fill-current" viewBox="0 0 24 24">
							<path
								d="M18 21l-4-4h3V7h-3l4-4 4 4h-3v10h3M2
								19v-2h10v2M2 13v-2h7v2M2 7V5h4v2H2z"></path>
						</svg>
					</button>
				</div>
            </div>
            <div class="col-span-12 my-5 mx-10">
                <div class="grid gap-2 grid-cols-1 lg:grid-cols-1">
                    <div class="bg-white p-4 shadow-lg rounded-lg">
                       
                        <!-- <h1 class="font-bold text-base ml-5">Products</h1> -->
                        <div class="mt-4">
                            <div class="flex flex-col">
                                <div class="-my-2 overflow-x-auto">
                                    <div class="py-2 align-middle inline-block min-w-full">
                                        <div
                                            class="shadow overflow-hidden border-b border-gray-200 sm:rounded-lg bg-white">
                                            <table class="min-w-full divide-y divide-gray-200">
                                                <thead>
                                                    <tr>
                                                        <th
                                                            class="px-6 py-3 bg-gray-50 text-xs leading-4 font-medium text-gray-500 uppercase tracking-wider">
                                                            <div class="flex cursor-pointer">
                                                                <span class="mr-2">PRODUCT NAME</span>
                                                            </div>
                                                        </th>
                                                        <th
                                                            class="px-6 py-3 bg-gray-50 text-xs leading-4 font-medium text-gray-500 uppercase tracking-wider">
                                                            <div class="flex cursor-pointer">
                                                                <span class="mr-2">Customer </span>
                                                            </div>
                                                        </th>
                                                        <th
                                                            class="px-6 py-3 bg-gray-50 text-xs leading-4 font-medium text-gray-500 uppercase tracking-wider">
                                                            <div class="flex cursor-pointer">
                                                                <span class="mr-2">Amount</span>
                                                            </div>
                                                        </th>
                                                        <th
                                                            class="px-6 py-3 bg-gray-50 text-xs leading-4 font-medium text-gray-500 uppercase tracking-wider">
                                                            <div class="flex cursor-pointer">
                                                                <span class="mr-2">ACTION</span>
                                                            </div>
                                                        </th>
                                                    </tr>
                                                </thead>
                                                <tbody class="bg-white divide-y divide-gray-200">
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                   <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                              
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                               
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>'<tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                               
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                               
                                                            </div>
                                                        </td>
                                                    </tr>
                                                    <tr>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex items-center">
                                                                <div class="mr-2">
                                                                    <img class="w-12 h-12 rounded-full" src="https://randomuser.me/api/portraits/men/1.jpg"/>
                                                                </div>
                                                                <p>Apple MacBook Pro 13</p>
                                                            <!-- <p class="text-xs text-gray-400">PC & Laptop
                                                            </p> -->
                                                                
                                                            </div>
                                                          
                                                            
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <p>77</p>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex text-green-500">
                                                                <svg xmlns="http://www.w3.org/2000/svg"
                                                                    class="w-5 h-5 mr-1" fill="none"
                                                                    viewBox="0 0 24 24"
                                                                    stroke="currentColor">
                                                                    <path stroke-linecap="round"
                                                                        stroke-linejoin="round"
                                                                        stroke-width="2"
                                                                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                                                </svg>
                                                                <p>Active</p>
                                                            </div>
                                                        </td>
                                                        <td
                                                            class="px-6 py-4 whitespace-no-wrap text-sm leading-5">
                                                            <div class="flex space-x-4">
                                                                <button href="#" class="text-green-500 hover:text-green-800">
                                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                                                </svg>
                                                                <p>View</p>
                                                                </button>
                                                                
                                                            </div>
                                                        </td>
                                                    </tr>
                                                </tbody>
                                            </table>
                                        </div>
                                        <div
                                        class="px-5 py-5 bg-white border-t flex flex-col xs:flex-row items-center xs:justify-between          ">
                                        <span class="text-xs xs:text-sm text-gray-900">
                                            Showing 1 to 4 of 50 Entries
                                        </span>
                                        <div class="inline-flex mt-2 xs:mt-0">
                                            <button
                                                class="text-sm bg-gray-300 hover:bg-gray-400 text-gray-800 font-semibold py-2 px-4 rounded-l">
                                                Prev
                                            </button>
                                            <button
                                                class="text-sm bg-gray-300 hover:bg-gray-400 text-gray-800 font-semibold py-2 px-4 rounded-r">
                                                Next
                                            </button>
                                        </div>
                                    </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
          <DashFooter />
        </div>
      </div>
    </div>
</template>