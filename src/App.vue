<template>
  <div class="relative bg-white overflow-hidden">
    <div class="hidden lg:block lg:absolute lg:inset-0" aria-hidden="true">
      <svg class="absolute top-0 left-1/2 transform translate-x-64 -translate-y-8" width="640" height="784" fill="none" viewBox="0 0 640 784">
        <defs>
          <pattern id="9ebea6f4-a1f5-4d96-8c4e-4c2abf658047" x="118" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
            <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
          </pattern>
        </defs>
        <rect y="72" width="640" height="640" class="text-gray-50" fill="currentColor" />
        <rect x="118" width="404" height="784" fill="url(#9ebea6f4-a1f5-4d96-8c4e-4c2abf658047)" />
      </svg>
    </div>

    <div class="relative pt-6 pb-16 sm:pb-24 lg:pb-32">
      <Popover>
        <nav class="relative max-w-7xl mx-auto flex items-center justify-between px-4 sm:px-6" aria-label="Global">
          <div class="flex items-center flex-1">
            <div class="flex items-center justify-between w-full md:w-auto">
              <a href="#">
                <span class="sr-only">WolfProductions</span>
                <img class="h-8 w-auto sm:h-10" :src="logo" alt="WolfProductions logo" />
              </a>
              <div class="-mr-2 flex items-center md:hidden">
                <PopoverButton class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-red-500">
                  <span class="sr-only">Open main menu</span>
                  <MenuIcon class="h-6 w-6" aria-hidden="true" />
                </PopoverButton>
              </div>
            </div>
            <div class="hidden md:block md:ml-10 md:space-x-10">
              <a v-for="item in navigation" :key="item.name" :href="item.href" class="font-medium text-gray-500 hover:text-gray-900">{{ item.name }}</a>
            </div>
          </div>
          <!-- <div class="hidden md:block text-right">
            <span class="inline-flex rounded-md shadow-md ring-1 ring-black ring-opacity-5">
              <a href="#" class="inline-flex items-center px-4 py-2 border border-transparent text-base font-medium rounded-md text-red-600 bg-white hover:bg-gray-50"> Log in </a>
            </span>
          </div> -->
        </nav>

        <PopoverPanel focus class="absolute z-10 top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden">
          <div class="rounded-lg shadow-md bg-white ring-1 ring-black ring-opacity-5 overflow-hidden">
            <div class="px-5 pt-4 flex items-center justify-between">
              <div>
                <img class="h-8 w-auto" :src="logo" alt="" />
              </div>
              <div class="-mr-2">
                <PopoverButton class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-red-500">
                  <span class="sr-only">Close main menu</span>
                  <XIcon class="h-6 w-6" aria-hidden="true" />
                </PopoverButton>
              </div>
            </div>
            <div class="px-2 pt-2 pb-3 space-y-1">
              <a v-for="item in navigation" :key="item.name" :href="item.href" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">{{ item.name }}</a>
            </div>
            <!-- <a href="#" class="block w-full px-5 py-3 text-center font-medium text-red-600 bg-gray-50 hover:bg-gray-100"> Log in </a> -->
          </div>
        </PopoverPanel>
      </Popover>

      <main class="mt-16 mx-auto max-w-7xl px-4 sm:mt-24 sm:px-6 lg:mt-32">
        <div class="lg:grid lg:grid-cols-12 lg:gap-8">
          <div class="sm:text-center md:max-w-2xl md:mx-auto lg:col-span-7 lg:text-left">
            <h1>
              <span class="block text-sm font-semibold uppercase tracking-wide text-gray-500 sm:text-base lg:text-sm xl:text-base">Hi there 👋</span>
              <span class="mt-1 block text-4xl tracking-tight font-extrabold sm:text-5xl xl:text-6xl">
                <span class="block text-gray-900">My name is</span>
                <span class="block text-red-600">Ivan de Wolf</span>
              </span>
            </h1>
            <p class="text-base mt-3 text-gray-500 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl">an enthousiastic and hardworking self-employed. I love realizing new ideas. I've done a lot of work on software and recently became a certified voice actor. Check out my work for each category.</p>
            <p class="mt-3 text-base text-gray-500 sm:text-xl lg:text-lg xl:text-xl">
              <a href="#software" class="hover:underline block"><strong>🖥 Software Engineer</strong></a>
              <a href="#voice" class="hover:underline block"><strong>🎙 Voice Actor</strong></a>
              <a href="#photographer" class="hover:underline block"><strong>📸 Photographer</strong></a>
            </p>
            <div class="mt-8 sm:max-w-lg sm:mx-auto sm:text-center lg:text-left lg:mx-0">
              <!-- <p class="text-base font-medium text-gray-900">Let's get into contact to realise your next idea!</p> -->
              <!-- <form action="#" method="POST" class="mt-3 sm:flex">
                <label for="email" class="sr-only">Email</label>
                <input type="email" name="email" id="email" class="block w-full py-3 text-base rounded-md placeholder-gray-500 shadow-sm focus:ring-red-500 focus:border-red-500 sm:flex-1 border-gray-300 sm:mr-3" placeholder="Enter your email" />
                <button type="submit" class="mt-3 w-full px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-gray-800 shadow-sm hover:bg-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 sm:mt-0 sm:flex-shrink-0 sm:inline-flex sm:items-center sm:w-auto">Contact me</button>
              </form> -->
            </div>
          </div>
          <div class="mt-12 relative sm:max-w-lg sm:mx-auto lg:mt-0 lg:max-w-none lg:mx-0 lg:col-span-5 lg:flex lg:items-center">
            <svg class="absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-8 scale-75 origin-top sm:scale-100 lg:hidden" width="640" height="784" fill="none" viewBox="0 0 640 784" aria-hidden="true">
              <defs>
                <pattern id="4f4f415c-a0e9-44c2-9601-6ded5a34a13e" x="118" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                  <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                </pattern>
              </defs>
              <rect y="72" width="640" height="640" class="text-gray-50" fill="currentColor" />
              <rect x="118" width="404" height="784" fill="url(#4f4f415c-a0e9-44c2-9601-6ded5a34a13e)" />
            </svg>
            <div class="relative mx-auto w-full rounded-lg shadow-lg lg:max-w-xs">
              <img class="relative block w-full rounded-lg overflow-hidden" :src="ivan" alt="" />
            </div>
          </div>
        </div>
      </main>
    </div>

    <!-- Software engineer -->
    <div class="relative bg-gray-50 pt-8 pb-20 px-4 sm:px-6 lg:pt-16 lg:pb-28 lg:px-8">
      <div class="absolute inset-0">
        <div class="bg-white h-1/3 sm:h-2/3" />
      </div>
      <div class="relative max-w-7xl mx-auto">
        <div class="text-center">
          <h2 id="showcase" class="text-base font-semibold tracking-wider text-red-600 uppercase">Software engineer</h2>
          <h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">Software to experience</h2>
          <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4">These projects are some of the work I did. Some of them for a client and some are just for personal experience.</p>
        </div>
        <div class="mt-12 max-w-lg mx-auto grid gap-5 lg:grid-cols-4 lg:max-w-none">
          <a :href="post.href" target="_blank" v-for="post in softwareProjects" :key="post.title" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-video" :src="post.imageUrl" alt="" />
            </div>
            <div class="flex-1 bg-white p-6 flex flex-col justify-between">
              <div class="flex-1">
                <p class="text-sm font-medium text-red-600">
                  <span>
                    {{ post.category.name }}
                  </span>
                </p>
                <div class="block mt-2">
                  <p class="text-xl font-semibold text-gray-900">
                    {{ post.title }}
                  </p>
                  <p class="mt-3 text-base text-gray-500">
                    {{ post.description }}
                  </p>
                </div>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>

    <!-- <div class="py-16 bg-gray-50 overflow-hidden lg:py-24">
      <div class="relative max-w-xl mx-auto px-4 sm:px-6 lg:px-8 lg:max-w-7xl">
        <svg class="hidden lg:block absolute left-full transform -translate-x-1/2 -translate-y-1/4" width="404" height="784" fill="none" viewBox="0 0 404 784" aria-hidden="true">
          <defs>
            <pattern id="b1e6e422-73f8-40a6-b5d9-c8586e37e0e7" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#b1e6e422-73f8-40a6-b5d9-c8586e37e0e7)" />
        </svg>

        <div class="relative">
          <h2 class="text-center text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">Other experience</h2>
          <p class="mt-4 max-w-3xl mx-auto text-center text-xl text-gray-500">Besides some webapplications I've also worked on some other software projects.</p>
        </div>

        <div class="relative mt-12 lg:mt-24 lg:grid lg:grid-cols-2 lg:gap-8 lg:items-center">
          <div class="relative">
            <h3 class="text-2xl font-extrabold text-gray-900 tracking-tight sm:text-3xl">Escaperooms</h3>
            <p class="mt-3 text-lg text-gray-500">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur minima sequi recusandae, porro maiores officia assumenda aliquam laborum ab aliquid veritatis impedit odit adipisci optio iste blanditiis facere. Totam, velit.</p>

            <dl class="mt-10 space-y-10">
              <div v-for="item in transferFeatures" :key="item.id" class="relative">
                <dt>
                  <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                    <component :is="item.icon" class="h-6 w-6" aria-hidden="true" />
                  </div>
                  <p class="ml-16 text-lg leading-6 font-medium text-gray-900">{{ item.name }}</p>
                </dt>
                <dd class="mt-2 ml-16 text-base text-gray-500">
                  {{ item.description }}
                </dd>
              </div>
            </dl>
          </div>

          <div class="mt-10 -mx-4 relative lg:mt-0" aria-hidden="true">
            <svg class="absolute left-1/2 transform -translate-x-1/2 translate-y-16 lg:hidden" width="784" height="404" fill="none" viewBox="0 0 784 404">
              <defs>
                <pattern id="ca9667ae-9f92-4be7-abcb-9e3d727f2941" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                  <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                </pattern>
              </defs>
              <rect width="784" height="404" fill="url(#ca9667ae-9f92-4be7-abcb-9e3d727f2941)" />
            </svg>
            <img class="relative mx-auto" width="490" src="https://tailwindui.com/img/features/feature-example-1.png" alt="" />
          </div>
        </div>
      </div>
    </div> -->

    <!-- Voice actor -->
    <div class="py-16 bg-gray-50 overflow-hidden lg:py-24">
      <div class="relative max-w-xl mx-auto px-4 sm:px-6 lg:px-8 lg:max-w-7xl">
        <div class="text-center">
          <h2 id="voice" class="text-base font-semibold tracking-wider text-red-600 uppercase">Voice actor</h2>
          <h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">Using my voice to tell a story</h2>
          <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4">Let's give your project a professional voice-over. Stemacteren.nl&nbsp;Certified® with my own studio at home.</p>
        </div>

        <svg class="hidden lg:block absolute right-full transform translate-x-1/2 translate-y-12" width="404" height="784" fill="none" viewBox="0 0 404 784" aria-hidden="true">
          <defs>
            <pattern id="64e643ad-2176-4f86-b3d7-f2c5da3b6a6d" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#64e643ad-2176-4f86-b3d7-f2c5da3b6a6d)" />
        </svg>

        <div class="relative mt-12 sm:mt-16 lg:mt-24">
          <div class="lg:grid lg:grid-flow-row-dense lg:grid-cols-2 lg:gap-8 lg:items-center">
            <div class="lg:col-start-2">
              <h3 class="text-2xl font-extrabold text-gray-900 tracking-tight sm:text-3xl">Demo recordings</h3>
              <p class="mt-3 text-lg text-gray-500">These are some demo recordings of my voice. Let's hear if my voice matches your next project!</p>

              <dl class="mt-10 space-y-10">
                <div class="relative">
                  <dt>
                    <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                      <MicrophoneIcon class="h-6 w-6" aria-hidden="true" />
                    </div>
                    <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Demo 1</p>
                  </dt>
                  <dd class="mt-0 ml-16 text-base text-gray-500">
                    <p class="mb-1">This is the first demo with recordings of a commercial for a vacation spot (corendon), coffee (Douwe Egberts), a narrative about a research television program (Zembla), commercial for health insurance check (Independer), and an education video narrative (Athene).</p>
                    <audio controls="controls" class="w-full h-7" :src="demo1" />
                  </dd>
                </div>
                <div class="relative">
                  <dt>
                    <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                      <MicrophoneIcon class="h-6 w-6" aria-hidden="true" />
                    </div>
                    <p class="ml-16 text-lg leading-6 font-medium text-gray-900">Demo 2</p>
                  </dt>
                  <dd class="mt-0 ml-16 text-base text-gray-500">
                    <p class="mb-1">This is the second demo with recordings of a commercial for a vacation spot, garden shop, and a narative about DNA.</p>
                    <audio controls="controls" class="w-full h-7" :src="demo2" />
                  </dd>
                </div>
              </dl>
            </div>

            <div class="mt-10 -mx-4 relative lg:mt-0 lg:col-start-1">
              <svg class="absolute left-1/2 transform -translate-x-1/2 translate-y-16 lg:hidden" width="784" height="404" fill="none" viewBox="0 0 784 404" aria-hidden="true">
                <defs>
                  <pattern id="e80155a9-dfde-425a-b5ea-1f6fadd20131" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                    <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                  </pattern>
                </defs>
                <rect width="784" height="404" fill="url(#e80155a9-dfde-425a-b5ea-1f6fadd20131)" />
              </svg>
              <div class="px-4">
                <div class="relative mx-auto w-full rounded-lg shadow-lg lg:max-w-xs">
                  <img class="relative block w-full rounded-lg overflow-hidden" :src="voice" alt="" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Photographer -->
    <div class="relative bg-gray-50 pt-8 pb-20 px-4 sm:px-6 lg:pt-16 lg:pb-28 lg:px-8">
      <div class="absolute inset-0">
        <div class="bg-white h-1/3 sm:h-2/3" />
      </div>
      <div class="relative max-w-7xl mx-auto">
        <div class="text-center">
          <h2 id="photographer" class="text-base font-semibold tracking-wider text-red-600 uppercase">Photographer</h2>
          <h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">Creating memories that last forever</h2>
          <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4">I love to record memories from all kinds of different moments from people. From a concert, gala, festival, and vacation. You can click on the picture to see that entire album.</p>
        </div>
        <div class="mt-12 max-w-lg mx-auto grid gap-5 lg:grid-cols-4 lg:max-w-none">
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62b9d3530c2dd7b6b0cf54fa/62be091ca6005a34897d4ca1" class="flex flex-col row-span-2 rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[2/3] object-cover" :src="photo1" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62b9d3530c2dd7b6b0cf54fa/62d7fc6244c779c8f7fe1ed9" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[3/2] object-cover" :src="photo2" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62d7fdc2fbdc03eadce34496/62d7feb744c779c8f7fe1ef8" class="flex flex-col row-span-2 rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[2/3] object-cover" :src="photo3" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62b996d9b0ebe5c6db10f734/62d801b444c779c8f7fe1f0c" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[3/2] object-cover" :src="photo4" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62b996d9b0ebe5c6db10f734/62d4559a44c779c8f7fe1c55" class="flex flex-col row-span-2 rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[2/3] object-cover" :src="photo5" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62d7fdc2fbdc03eadce34496/62d804bd44c779c8f7fe1f28" class="flex flex-col row-span-2 rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[2/3] object-cover" :src="photo6" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62d7fdc2fbdc03eadce34496/62d804bd44c779c8f7fe1f28" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[3/2] object-cover" :src="photo7" />
            </div>
          </a>
          <a target="_blank" rel="noopener noreferrer" href="https://wolfproductions.photos/62d81ba2fbdc03eadce34497/62d81cf644c779c8f7fe1f3e" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
            <div class="flex-shrink-0">
              <img class="w-full aspect-[3/2] object-cover" :src="photo8" />
            </div>
          </a>
        </div>
      </div>
    </div>

    <!-- This is me -->
    <div class="py-16 bg-gray-50 overflow-hidden lg:py-24">
      <div class="relative max-w-xl mx-auto px-4 sm:px-6 lg:px-8 lg:max-w-7xl">
        <div class="text-center">
          <h2 id="aboutme" class="text-base font-semibold tracking-wider text-red-600 uppercase">This is me</h2>
          <h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">Hi there! Let me introduce myself</h2>
          <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4"></p>
        </div>
        <svg class="hidden lg:block absolute left-full transform -translate-x-1/2 -translate-y-1/4" width="404" height="784" fill="none" viewBox="0 0 404 784" aria-hidden="true">
          <defs>
            <pattern id="b1e6e422-73f8-40a6-b5d9-c8586e37e0e7" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#b1e6e422-73f8-40a6-b5d9-c8586e37e0e7)" />
        </svg>

        <div class="relative mt-12 sm:mt-16 lg:mt-24">
          <div class="lg:grid lg:grid-flow-row-dense lg:grid-cols-2 lg:gap-8 lg:items-center">
            <div>
              <h3 class="text-2xl font-extrabold text-gray-900 tracking-tight sm:text-3xl">About me</h3>
              <p class="mt-3 text-lg text-gray-500">As you can see, I keep myself busy with a lot of things. But that is exactly what I like: combining lots of fun, great and awesome projects. Let talk about your next project!</p>
              <ul role="list" class="flex space-x-5 mt-4">
                <li>
                  <a href="#" class="text-gray-400 hover:text-gray-500">
                    <span class="sr-only">Twitter</span>
                    <svg class="w-5 h-5" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20">
                      <path d="M6.29 18.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0020 3.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.073 4.073 0 01.8 7.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 010 16.407a11.616 11.616 0 006.29 1.84" />
                    </svg>
                  </a>
                </li>
                <li>
                  <a href="#" class="text-gray-400 hover:text-gray-500">
                    <span class="sr-only">LinkedIn</span>
                    <svg class="w-5 h-5" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.338 16.338H13.67V12.16c0-.995-.017-2.277-1.387-2.277-1.39 0-1.601 1.086-1.601 2.207v4.248H8.014v-8.59h2.559v1.174h.037c.356-.675 1.227-1.387 2.526-1.387 2.703 0 3.203 1.778 3.203 4.092v4.711zM5.005 6.575a1.548 1.548 0 11-.003-3.096 1.548 1.548 0 01.003 3.096zm-1.337 9.763H6.34v-8.59H3.667v8.59zM17.668 1H2.328C1.595 1 1 1.581 1 2.298v15.403C1 18.418 1.595 19 2.328 19h15.34c.734 0 1.332-.582 1.332-1.299V2.298C19 1.581 18.402 1 17.668 1z" clip-rule="evenodd" />
                    </svg>
                  </a>
                </li>
              </ul>

              <form action="#" method="POST" class="mt-4 sm:flex">
                <label for="email" class="sr-only">Email</label>
                <input type="email" name="email" id="email" class="block w-full py-3 text-base rounded-md placeholder-gray-500 shadow-sm focus:ring-red-500 focus:border-red-500 sm:flex-1 border-gray-300 sm:mr-3" placeholder="Enter your email" />
                <a href="mailto:ivan@wolfproductions.dev" class="mt-3 w-full px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-gray-800 shadow-sm hover:bg-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 sm:mt-0 sm:flex-shrink-0 sm:inline-flex sm:items-center sm:w-auto">Contact me</a>
              </form>
            </div>

            <div class="mt-10 -mx-4 relative lg:mt-0">
              <svg class="absolute left-1/2 transform -translate-x-1/2 translate-y-16 lg:hidden" width="784" height="404" fill="none" viewBox="0 0 784 404" aria-hidden="true">
                <defs>
                  <pattern id="e80155a9-dfde-425a-b5ea-1f6fadd20131" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                    <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                  </pattern>
                </defs>
                <rect width="784" height="404" fill="url(#e80155a9-dfde-425a-b5ea-1f6fadd20131)" />
              </svg>
              <div class="px-4">
                <div class="relative mx-auto w-full rounded-lg shadow-lg lg:max-w-xs">
                  <img class="relative block w-full rounded-lg overflow-hidden" :src="photo" alt="" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { MenuIcon, XIcon, GlobeAltIcon, LightningBoltIcon, ScaleIcon, MicrophoneIcon } from '@heroicons/vue/outline'

import logo from './assets/white_text_bg.svg'
import ivan from './assets/ivan.jpg'
import voice from './assets/voice.jpg'
import photo from './assets/photo.jpg'
import demo1 from './assets/audio/demo1.wav'
import demo2 from './assets/audio/demo2.mp3'

import periodictable from './assets/screenshots/periodic_table.jpg'
import nsplanner from './assets/screenshots/ns_reisplanner.jpg'
import ticketvise from './assets/screenshots/ticketvise.jpg'
import tlc_era from './assets/screenshots/tlc_era.jpg'
import weerwolven from './assets/screenshots/weerwolven.png'
import formula1 from './assets/screenshots/formula1.jpg'
import ufo_stam from './assets/screenshots/ufo-stam.jpg'

import photo1 from './assets/images/blue_king-102.jpg'
import photo2 from './assets/images/diplomauitreiking_2021-138.jpg'
import photo3 from './assets/images/eersteborrel_2021-15.jpg'
import photo4 from './assets/images/SSN_Gala_2022-011.jpg'
import photo5 from './assets/images/svia_flux_2022-129.jpg'
import photo6 from './assets/images/Cyprus_2022-276.jpg'
import photo7 from './assets/images/promocie_strasbourg-251.jpg'
import photo8 from './assets/images/svia_flux_2022-050.jpg'

const navigation = [
  { name: 'Software Engineer', href: '#software' },
  { name: 'Voice Actor', href: '#voice' },
  { name: 'Photography', href: '#photographer' },
  { name: 'This is me', href: '#aboutme' },
  { name: 'Contact', href: '#contact' },
]

const transferFeatures = [
  {
    id: 1,
    name: 'Competitive exchange rates',
    description:
      'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.',
    icon: GlobeAltIcon,
  },
  {
    id: 2,
    name: 'No hidden fees',
    description:
      'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.',
    icon: ScaleIcon,
  },
  {
    id: 3,
    name: 'Transfers are instant',
    description:
      'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.',
    icon: LightningBoltIcon,
  },
]

const softwareProjects = [
  {
    title: 'TicketVise',
    href: 'https://ticketvise.com/',
    category: { name: 'Co-Founder', href: '#' },
    description: 'A startup that improves communication between students and teachers while presenting intelligent insights.',
    imageUrl: ticketvise
  },
  {
    title: 'TLC ERA-tool',
    href: 'https://tlc-uva.github.io/educational-redesign-aid/',
    category: { name: 'Developer', href: '#' },
    description: 'Project for the University of Amsterdam. The tool is used by teachers to help them design their classes digitally.',
    imageUrl: tlc_era
  },
  {
    title: 'Interactive Periodic Table',
    href: 'https://periodictable.ivandewolf.nl/',
    category: { name: 'Interactive', href: '#' },
    description: 'Interactive tool to show the periodic table and its elements. Fun project I did in my spare time.',
    imageUrl: periodictable
  },
  {
    title: 'NS departure times',
    href: 'http://ns.ivandewolf.nl/',
    category: { name: 'API', href: '#' },
    description: 'Using the NS API to show the departure times of the NS, just like they do on their departure boards.',
    imageUrl: nsplanner
  },
  {
    title: 'Weerwolven online',
    href: '',
    category: { name: 'Creator', href: '' },
    description: 'Based on the cardgame Weerwolven, this is a webapp to play the game online.',
    imageUrl: weerwolven
  },
  {
    title: 'Formula 1 Dashboard',
    href: '',
    category: { name: 'Implementation', href: '' },
    description: 'Created a dashboard based on a design found online.',
    imageUrl: formula1
  },
  {
    title: 'U.F.O.-Stam website',
    href: '',
    category: { name: 'Creator', href: '' },
    description: 'Designed and created a website for the U.F.O.-Stam.',
    imageUrl: ufo_stam
  },
]
</script>
