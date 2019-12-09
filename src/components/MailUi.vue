<template>
  <div>
      <link rel="stylesheet" 
        href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" 
        integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" 
        crossorigin="anonymous">
    <div class="h-screen flex flex-col">
        <header class="flex flex-shrink-0">
            <div class="w-64 flex-shrink-0 px-4 py-3 bg-gray-800">
                <button class="flex items-center">
                    <img 
                        class=" h-8 w-8 rounded-full object-cover"
                        src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=faceareap=4&w=144&q=60" 
                        alt="">
                    <span class="ml-4 text-sm font-medium text-white">Adjaloko Edward </span>
                    <svg 
                        class="ml-10 h-6 w-6 stroke-current text-gray-400" 
                        viewbox="0 0 24 24">
                       <path d="M16 10l-4 4-4-4" 
                            stroke-width="2" 
                            stroke-linecap="round" 
                            stroke-linejoin="round"/>
                    </svg>
                </button>
            </div>
            <div class="flex-1 flex items-center justify-between bg-gray-700 px-6">
                <div class="">
                    <nav class="flex">
                        <a href="" 
                           class="ml-2 inline-block leading-none rounded-lg bg-gray-800 px-3 py-2 text-sm font-medium text-white hover:bg-gray-600">
                           Mailbox
                        </a>
                        <a href="" 
                           class="ml-2 inline-block leading-none rounded-lg px-3 py-2 text-sm font-medium text-white hover:bg-gray-600">
                           Customers
                        </a>
                        <a href="" 
                           class="ml-2 inline-block leading-none rounded-lg px-3 py-2 text-sm font-medium text-white hover:bg-gray-600">
                           Reporting
                        </a>
                        <a href="" 
                           class="ml-2 inline-block leading-none rounded-lg px-3 py-2 text-sm font-medium text-white hover:bg-gray-600">
                           Manage
                        </a>
                    </nav>
                </div>
                
                <div class=""></div>
                <div class="flex items-center">
                    <div class="relative w-64">
                        <span class="absolute inset-y-0 flex items-center left-0 pl-2">
                        <i class="fas fa-search h-5 w-5 mr-2 text-gray-500" style="font-size: 20px;"></i>
                        </span>
                        
                        <input class="block pl-8 pr-4 py-2 leading-tight width-full w-64 bg-gray-900 rounded-lg  text-sm placeholder-gray-400 text-white focus:bg-white focus:placeholder-gray-600 focus:text-gray-900 focus:outline-none" placeholder="Search">
                    </div>
                        
                        <button class="text-gray-400 ml-4 hover:text-gray-200">
                                <i class="far fa-bell h-5 w-5 text-gray-400" style="font-size: 20px;"></i>
                        </button>
                        <button class="text-gray-400 ml-4 hover:text-gray-200">
                           <i class="far fa-question-circle h-5 w-5 text-gray-400" style="font-size: 20px;"></i>
                        </button>
                    </div>
            </div>  
        </header>
        
        <div class="flex-1 flex bg-gray-200 overflow-hidden">
          <vue-custom-scrollbar class="scroll-area"  :settings="settings" @ps-scroll-y="scrollHanle">
           <div class="w-64 p-6 bg-gray-100 overflow-y-auto">
              <nav>
                  <h2 
                  class="text-sm font-semibold text-gray-600 tracking-wide uppercase">
                  Mailboxes
                  </h2>
                  <div class="mt-3">
                      <a href="" class="-mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between bg-red-200 rounded-lg">
                      <span class="inline-flex"> 
                            <i class="fas fa-inbox text-red-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-red-500">Inbox</span>
                      </span>
                      <span class="inline-block px-4 leading-none py-1 text-xs font-semibold text-red-700 bg-red-300 rounded-full">
                          6
                      </span>
                  </a>

                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex">      
                              <i class="far fa-flag text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Flagged</span>
                      </span>
                      <!-- <span class="inline-block px-4 leading-none py-1 text-xs font-semibold text-gray-700 bg-gray-300 rounded-full">
                          6
                      </span> -->
                  </a>

                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex"> 
                            <i class="far fa-edit text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Drafts</span>
                      </span>
                      <span class="inline-block px-4 leading-none py-1 text-xs font-semibold text-gray-700 bg-gray-300 rounded-full">
                          2
                      </span>
                  </a>

                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex"> 
                           <i class="far fa-user-circle text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Assigned</span>
                      </span>
                      <span class="inline-block px-4 leading-none py-1 text-xs font-semibold text-gray-700 bg-gray-300 rounded-full">
                          1
                      </span>
                  </a>
                    <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex"> 
                           <i class="far fa-envelope text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">All Mail</span>
                      </span>
                      
                  </a>

                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex"> 
                          <i class="far fa-check-circle text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Closed</span>
                      </span>
                      <!-- <span class="inline-block px-4 leading-none py-1 text-xs font-semibold text-gray-700 bg-gray-300 rounded-full">
                          6
                      </span> -->
                  </a>
                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex"> 
                           <i class="far fa-trash-alt text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Junk</span>
                      </span>
                  </a>
                    
                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex items-center"> 
                            <i class="far fa-paper-plane pt-1 text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Sent</span>
                      </span>
                      
                  </a>
                  <a href="" class="mt-2 -mx-3 px-3 py-2 text-sm font-medium flex items-center justify-between hover:bg-gray-200 rounded-lg">
                      <span class="inline-flex items-center"> 
                            <i class="fas fa-wrench pt-1 text-gray-500 h-6 w-6" style="font-size: 20px;"></i>
                            <span class="ml-2 text-gray-700">Settings</span>
                      </span>
                      
                  </a>
                  </div>
                  <h2 
                  class="mt-8 text-sm font-semibold text-gray-600 tracking-wide uppercase">
                  Folders
                  </h2>
                  <div class="mt-4">
                    <a href="" class="block text-sm font-medium text-gray-700">Refund</a>
                    <a href="" class="mt-4 block text-sm font-medium text-gray-700">Discount</a>
                    <a href="" class="mt-4 block text-sm font-medium text-gray-700">Bugs</a>
                  </div>
                  
              </nav>
           </div>
           
          </vue-custom-scrollbar>
        
        <main class="flex-1 flex bg-gray-200">
            <div class="relative flex flex-col w-full max-w-xs flex-grow border-l border-r bg-gray-200">
                <div class="flex-shrink-0 px-4 py-2 flex items-center justify-between border-b">
                 <button class="flex items-center text-sm font-semibold text-gray-600">
                    Sorted by Date
                    <svg aria-hidden="true" class="svg-inline--fa fa-chevron-down fa-w-14 ml-2 h-3  w-6 fill-current text-gray-500" data-icon="chevron-down" data-prefix="fas" viewBox="0 0 448 512">
                    <defs/>
                    <path  d="M207.029 381.476L12.686 187.132c-9.373-9.373-9.373-24.569 0-33.941l22.667-22.667c9.357-9.357 24.522-9.375 33.901-.04L224 284.505l154.745-154.021c9.379-9.335 24.544-9.317 33.901.04l22.667 22.667c9.373 9.373 9.373 24.569 0 33.941L240.971 381.476c-9.373 9.372-24.569 9.372-33.942 0z"/>
                    </svg>
                 </button>
                 <button>
                     <svg aria-hidden="true" class="svg-inline--fa fa-sort-amount-up-alt fa-w-16 h-6 w-6 fill-current text-gray-500" data-icon="sort-amount-up-alt" data-prefix="fas" viewBox="0 0 512 512">
                        <defs/>
                        <path  d="M240 96h64a16 16 0 0016-16V48a16 16 0 00-16-16h-64a16 16 0 00-16 16v32a16 16 0 0016 16zm0 128h128a16 16 0 0016-16v-32a16 16 0 00-16-16H240a16 16 0 00-16 16v32a16 16 0 0016 16zm256 192H240a16 16 0 00-16 16v32a16 16 0 0016 16h256a16 16 0 0016-16v-32a16 16 0 00-16-16zm-256-64h192a16 16 0 0016-16v-32a16 16 0 00-16-16H240a16 16 0 00-16 16v32a16 16 0 0016 16zM16 160h48v304a16 16 0 0016 16h32a16 16 0 0016-16V160h48c14.21 0 21.39-17.24 11.31-27.31l-80-96a16 16 0 00-22.62 0l-80 96C-5.35 142.74 1.78 160 16 160z"/>
                        </svg>
                 </button>
            </div>
             <vue-custom-scrollbar class="scroll-area"  :settings="settings" @ps-scroll-y="scrollHanle">
            <div class="flex-1 overflow-y-auto">
                <a href="" class="block px-6 pt-3 pb-4 bg-gray-100 border-l-4 border-teal-400">
                    <div class="flex justify-between">
                        <span class="text-sm font-semibold text-gray-900">
                            Gloria Robertson
                            </span>
                        <span class="text-sm  text-gray-600">2 days ago</span>
                    </div>
                    <p class="text-sm font-semibold text-gray-900 ">Refund</p>
                    <p class="mt-2 text-sm text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, reprehenderit?</p>
                </a>
                <a href="" class="block px-6 pt-3 pb-4 bg-white border-t">
                    <div class="flex justify-between">
                        <span class="text-sm font-semibold text-gray-900">
                            Gloria Robertson
                            </span>
                        <span class="text-sm  text-gray-600">2 days ago</span>
                    </div>
                    <p class="text-sm font-semibold text-gray-900">Refund</p>
                    <p class="mt-2 text-sm text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, reprehenderit?</p>
                </a>
                <a href="" class="block px-6 pt-3 pb-4 bg-white border-t">
                    <div class="flex justify-between">
                        <span class="text-sm font-semibold text-gray-900">
                            Gloria Robertson
                            </span>
                        <span class="text-sm  text-gray-600">2 days ago</span>
                    </div>
                    <p class="text-sm font-semibold text-gray-900">Refund</p>
                    <p class="mt-2 text-sm text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, reprehenderit?</p>
                </a>
                <a href="" class="block px-6 pt-3 pb-4 bg-white border-t">
                    <div class="flex justify-between">
                        <span class="text-sm font-semibold text-gray-900">
                            Gloria Robertson
                            </span>
                        <span class="text-sm  text-gray-600">2 days ago</span>
                    </div>
                    <p class="text-sm font-semibold text-gray-900">Refund</p>
                    <p class="mt-2 text-sm text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, reprehenderit?</p>
                </a>
                <a href="" class="block px-6 pt-3 pb-4 bg-white border-t ">
                    <div class="flex justify-between">
                        <span class="text-sm font-semibold text-gray-900">
                            Gloria Robertson
                            </span>
                        <span class="text-sm  text-gray-600">2 days ago</span>
                    </div>
                    <p class="text-sm font-semibold text-gray-900">Refund</p>
                    <p class="mt-2 text-sm text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, reprehenderit?</p>
                </a>
                
            </div>
             </vue-custom-scrollbar>
            </div>
            <div class="flex-1 flex flex-col w-0">
                <div class="relative shadow-md">
                    <div class="flex items-center justify-between bg-gray-100 px-5 py-4 border-b">
                        <div class="flex items-center mt-2">
                            <a href="" class="ml-4">
                                <i class="fas fa-reply h-8 w-8 text-gray-500 " style="font-size: 20px;"></i>
                            </a>
                            <a href="" class="ml-4">
                               <i class="far fa-user-circle text-gray-500 h-8 w-8 " style="font-size: 20px;"></i>
                            </a>
                            <a href="" class="ml-4">
                               <i class="far fa-folder-open h-8 w-8 text-gray-500 " style="font-size: 20px;"></i>
                            </a>
                            <a href="" class="ml-4">
                              <i class="fas fa-ellipsis-h h-8 w-8 text-gray-500 " style="font-size: 20px;"></i>
                            </a>
                            
                        </div>
                        <div class="flex items-center mt-2">
                            <a href="" class="ml-2">
                                <i class="fas fa-chevron-down h-8 w-8 text-gray-500" style="font-size: 20px;"></i>
                            </a>
                             <a href="" class="ml-2">
                                <i class="fas fa-chevron-up h-8 w-8 text-gray-500" style="font-size: 20px;"></i>
                             </a>
                             
                        </div>                   
                    </div>
                    <div class="flex items-center justify-between bg-white px-5 py-4 ">
                        <h3 class="text-xl text-gray-900 truncate">Re: Student Discount?</h3>
                        <div class="ml-4 flex-shrink-0">
                            <span class="">#1428</span>
                            <span class="ml-2 text-sm font-semibold text-green-900 bg-gray-200 rounded-full leading-none px-2 py-1">Active</span>
                        </div>
                    </div>
                </div>
                <vue-custom-scrollbar class="scroll-area"  :settings="settings" @ps-scroll-y="scrollHanle">
                <div class="p-3 flex-1 overflow-y-auto">
                      <article class="mt-2 px-10 pt-6 pb-8 bg-white rounded-lg shadow">
                        <div class="flex items-center justify-between">
                            <p class="text-lg font-semibold">
                                <span class="text-gray-900">Joe Armstrong</span>
                                <span class="text-gray-600 ml-2">wrote</span>
                            </p>
                            <div class="flex items-center justify-between" >
                                <span class="text-sm text-gray-600">
                                    Yesterday at 7:24 AM
                                </span>
                                <img 
                                    class="ml-5 h-8 w-8 rounded-full object-cover"
                                    src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=faceareap=4&w=144&q=60" 
                                    alt="">
                            </div>
                        </div>
                        <div class="mt-6 text-gray-800 text-sm">
                            <p>Thanks so much! can`t wait to try it out</p>
                        </div>
                    </article>
                    <article class="mt-2 px-10 pt-6 pb-8 bg-white rounded-lg shadow">
                        <div class="flex items-center justify-between">
                            <p class="text-lg font-semibold">
                                <span class="text-gray-900">Monica White</span>
                                <span class="text-gray-600 ml-2">Replied</span>
                            </p>
                            <div class="flex items-center justify-between" >
                                <span class="text-sm text-gray-600">
                                    Yesterday at 7:24 AM
                                </span>
                                <img 
                                    class="ml-5 h-8 w-8 rounded-full object-cover"
                                    src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=faceareap=4&w=144&q=60" 
                                    alt="">
                            </div>
                        </div>
                        <div class="mt-6 text-gray-800 text-sm">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem vero fugit eaque est ad fuga illum quae vitae magni explicabo.</p>
                            <p class="mt-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente incidunt nulla maiores tempora. Optio velit aut eaque minus. Dignissimos, qui. Eos, impedit doloremque. Quaerat eos omnis voluptas vero tempore incidunt perferendis, architecto atque natus harum. Sapiente iusto eos recusandae commodi!</p>
                            <p class="mt-4 font-bold text-gray-900">Monica White</p>
                            <p>Customer Service</p>
                        </div>
                    </article>
                       <article class="mt-2 px-10 pt-6 pb-8 bg-white rounded-lg shadow">
                        <div class="flex items-center justify-between">
                            <p class="text-lg font-semibold">
                                <span class="text-gray-900">Joe Armstrong</span>
                                <span class="text-gray-600 ml-2">wrote</span>
                            </p>
                            <div class="flex items-center justify-between" >
                                <span class="text-sm text-gray-600">
                                    Yesterday at 7:24 AM
                                </span>
                                <img 
                                    class="ml-5 h-8 w-8 rounded-full object-cover"
                                    src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=faceareap=4&w=144&q=60" 
                                    alt="">
                            </div>
                        </div>
                        <div class="mt-6 text-gray-800 text-sm">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt placeat ullam recusandae praesentium, soluta harum.</p>
                        </div>
                    </article>
                </div>
                </vue-custom-scrollbar>
            </div>
        </main>
    </div>
        </div>
  </div>  
</template>
<script>
import '../assets/css/main.css'
import vueCustomScrollbar from 'vue-custom-scrollbar'
    export default {
        name: "MailUi",
         components: {
                vueCustomScrollbar
            },
            data() {
                return {
                settings: {
                    maxScrollbarLength: 60
                }
                }
            },
            methods: {
                scrollHanle() {
                // console.log(evt)
                }
            }
    }
</script>
<style scoped>
body {
  background-color: #edf2f7;
}
</style>