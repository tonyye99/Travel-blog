<template>
  <footer class="flex flex-col items-center px-5 py-5 mt-10 bg-blue-500">
    <div
      class="
        -mt-16
        w-11/12
        md:w-10/12
        xl:w-1/2
        px-5
        py-5
        flex flex-col
        md:justify-evenly md:flex-row
        items-center
        bg-white
        rounded-md
        md:space-x-5
        border-2
      "
    >
      <h2 class="font-bold text-blue-500 text-md md:text-xl">My Newsletter</h2>
      <div
        class="
          flex flex-col
          sm:flex-row
          space-x-2 space-y-5
          sm:space-y-0
          md:space-x-5
          pt-5
          md:pt-0
        "
      >
        <input
          class="
            shadow
            appearance-none
            border
            rounded
            w-full
            py-2
            px-3
            text-gray-700
            leading-tight
            focus:outline-none focus:shadow-outline
          "
          type="text"
          placeholder="Email"
        />
        <button
          class="
            bg-blue-500
            hover:bg-blue-700
            text-white
            font-bold
            py-2
            px-4
            rounded-full
          "
        >
          Subscribe
        </button>
      </div>
    </div>
    <div class="flex flex-col md:flex-row mt-10 space-y-5 md:space-y-0 md:space-x-5">
      <div class="flex flex-col items-center">
        <div><h2>Travello</h2></div>
        <div></div>
      </div>
      <div class="flex space-x-5">
        <div class="flex-col self-start">
          <h2 class="font-bold">Information</h2>
          <div class="mt-5 flex-col">
            <ul>
              <li>Home</li>
              <li>Blog</li>
              <li>About</li>
            </ul>
          </div>
        </div>
        <div class="flex-col self-start">
          <h2 class="font-bold">Contact</h2>
          <div class="mt-5 flex-col">
            <ul>
              <li>+959751841229</li>
              <li>ygxan18@gmail.com</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
