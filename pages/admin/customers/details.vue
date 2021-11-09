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
              <h1 class="text-2xl font-semibold">Customers</h1>

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
						placeholder="Search Customer..." />

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
                                            <div class="bg-white shadow overflow-hidden sm:rounded-lg">
                                                <div class="px-4 py-5 sm:px-6">
                                                <h3 class="text-lg leading-6 font-medium text-gray-900">
                                                    Applicant Information
                                                </h3>
                                                <p class="mt-1 max-w-2xl text-sm text-gray-500">
                                                    Personal details and application.
                                                </p>
                                                </div>
                                                <div class="border-t border-gray-200">
                                                <dl>
                                                    <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Full name
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        Margot Foster
                                                    </dd>
                                                    </div>
                                                    <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Application for
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        Backend Developer
                                                    </dd>
                                                    </div>
                                                    <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Email address
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        margotfoster@example.com
                                                    </dd>
                                                    </div>
                                                    <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Email address
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        margotfoster@example.com
                                                    </dd>
                                                    </div>
                                                    <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Email address
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        margotfoster@example.com
                                                    </dd>
                                                    </div>
                                                    <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Salary expectation
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        $120,000
                                                    </dd>
                                                    </div>
                                                    <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        About
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        Fugiat ipsum ipsum deserunt culpa aute sint do nostrud anim incididunt cillum culpa consequat. Excepteur qui ipsum aliquip consequat sint. Sit id mollit nulla mollit nostrud in ea officia proident. Irure nostrud pariatur mollit ad adipisicing reprehenderit deserunt qui eu.
                                                    </dd>
                                                    </div>
                                                    <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
                                                    <dt class="text-sm font-medium text-gray-500">
                                                        Attachments
                                                    </dt>
                                                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
                                                        <ul role="list" class="border border-gray-200 rounded-md divide-y divide-gray-200">
                                                        <li class="pl-3 pr-4 py-3 flex items-center justify-between text-sm">
                                                            <div class="w-0 flex-1 flex items-center">
                                                            <PaperClipIcon class="flex-shrink-0 h-5 w-5 text-gray-400" aria-hidden="true" />
                                                            <span class="ml-2 flex-1 w-0 truncate">
                                                                resume_back_end_developer.pdf
                                                            </span>
                                                            </div>
                                                            <div class="ml-4 flex-shrink-0">
                                                            <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">
                                                                Download
                                                            </a>
                                                            </div>
                                                        </li>
                                                        <li class="pl-3 pr-4 py-3 flex items-center justify-between text-sm">
                                                            <div class="w-0 flex-1 flex items-center">
                                                            <PaperClipIcon class="flex-shrink-0 h-5 w-5 text-gray-400" aria-hidden="true" />
                                                            <span class="ml-2 flex-1 w-0 truncate">
                                                                coverletter_back_end_developer.pdf
                                                            </span>
                                                            </div>
                                                            <div class="ml-4 flex-shrink-0">
                                                            <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">
                                                                Download
                                                            </a>
                                                            </div>
                                                        </li>
                                                        </ul>
                                                    </dd>
                                                    </div>
                                                </dl>
                                                </div>
                                            </div>
                                        </div>
                                        
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
          <DashFooter/>
        </div>
      </div>
    </div>
</template>