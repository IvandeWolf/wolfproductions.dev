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
                <img class="h-8 w-auto sm:h-10" :src="logo" alt="" />
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

        <transition enter-active-class="duration-150 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
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
        </transition>
      </Popover>

      <main class="mt-16 mx-auto max-w-7xl px-4 sm:mt-24 sm:px-6 lg:mt-32">
        <div class="lg:grid lg:grid-cols-12 lg:gap-8">
          <div class="sm:text-center md:max-w-2xl md:mx-auto lg:col-span-6 lg:text-left">
            <h1>
              <span class="block text-sm font-semibold uppercase tracking-wide text-gray-500 sm:text-base lg:text-sm xl:text-base">Hi there 👋</span>
              <span class="mt-1 block text-4xl tracking-tight font-extrabold sm:text-5xl xl:text-6xl">
                <span class="block text-gray-900">My name is</span>
                <span class="block text-red-600">Ivan de Wolf</span>
              </span>
            </h1>
            <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl">I'm a web developer and will help you make your idea reality. I've done my share of projects where I mainly focus on developing different websites and interfaces.</p>
            <div class="mt-8 sm:max-w-lg sm:mx-auto sm:text-center lg:text-left lg:mx-0">
              <p class="text-base font-medium text-gray-900">Get into contact to realise your next idea!</p>
              <form action="#" method="POST" class="mt-3 sm:flex">
                <label for="email" class="sr-only">Email</label>
                <input type="email" name="email" id="email" class="block w-full py-3 text-base rounded-md placeholder-gray-500 shadow-sm focus:ring-red-500 focus:border-red-500 sm:flex-1 border-gray-300" placeholder="Enter your email" />
                <button type="submit" class="mt-3 w-full px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-gray-800 shadow-sm hover:bg-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 sm:mt-0 sm:ml-3 sm:flex-shrink-0 sm:inline-flex sm:items-center sm:w-auto">Contact me</button>
              </form>
            </div>
          </div>
          <div class="mt-12 relative sm:max-w-lg sm:mx-auto lg:mt-0 lg:max-w-none lg:mx-0 lg:col-span-6 lg:flex lg:items-center">
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
              <img class="relative block w-full rounded-lg overflow-hidden " :src="ivan" alt="" />
            </div>
          </div>
        </div>
      </main>
    </div>

    <div class="relative bg-gray-50 pt-8 pb-20 px-4 sm:px-6 lg:pt-16 lg:pb-28 lg:px-8">
      <div class="absolute inset-0">
        <div class="bg-white h-1/3 sm:h-2/3" />
      </div>
      <div class="relative max-w-7xl mx-auto">
        <div class="text-center">
          <h2 id="showcase" class="text-base font-semibold tracking-wider text-red-600 uppercase">Showcase</h2>
          <h2 class="text-3xl tracking-tight font-extrabold text-gray-900 sm:text-4xl">Some awesome stuff I made</h2>
          <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4">These projects are some of the work I did. Some of them for a client and some are just for personal experience.</p>
        </div>
        <div class="mt-12 max-w-lg mx-auto grid gap-5 lg:grid-cols-4 lg:max-w-none">
          <a :href="post.href" target="_blank" v-for="post in posts" :key="post.title" class="flex flex-col rounded-lg shadow-lg overflow-hidden">
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
  </div>
</template>

<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { MenuIcon, XIcon } from '@heroicons/vue/outline'

import logo from './assets/white_text_bg.svg'
import ivan from './assets/ivan.jpg'

import periodictable from './assets/screenshots/periodic_table.jpg'
import nsplanner from './assets/screenshots/ns_reisplanner.jpg'
import ticketvise from './assets/screenshots/ticketvise.png'
import tlc_era from './assets/screenshots/tlc_era.jpg'
import weerwolven from './assets/screenshots/weerwolven.png'
import formula1 from './assets/screenshots/formula1.jpg'
import ufo_stam from './assets/screenshots/ufo-stam.jpg'

const navigation = [
  { name: 'Showcase', href: '#showcase' },
  { name: 'Experience', href: '#' },
  { name: 'Company', href: '#' },
  { name: 'Contact', href: '#' },
]

const posts = [
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
    title: 'Weerwolven online',
    href: '#',
    category: { name: 'Creator', href: '#' },
    description: 'Based on the cardgame Weerwolven, this is a webapp to play the game online.',
    imageUrl: weerwolven
  },
  {
    title: 'Formula 1 Dashboard',
    href: '#',
    category: { name: 'Implementation', href: '#' },
    description: 'Created a dashboard based on a design found online.',
    imageUrl: formula1
  },
  {
    title: 'U.F.O.-Stam website',
    href: '#',
    category: { name: 'Creator', href: '#' },
    description: 'Designed and created a website for the U.F.O.-Stam.',
    imageUrl: ufo_stam
  },
]
</script>
