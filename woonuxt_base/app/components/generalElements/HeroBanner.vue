<template>
  <div class="relative mx-auto">
    <NuxtImg
      width="1400"
      height="800"
      class="object-cover w-full h-[420px] lg:h-[560px] xl:h-[640px]"
      src="/images/main-banner.jpg"
      alt="בית החיות קריות"
      loading="eager"
      sizes="sm:100vw md:1400px lg:1920px xl:2560px"
      fetchpriority="high"
      preload
      placeholder
      placeholder-class="blur-xl" />
    <div class="container absolute inset-0 flex flex-col items-start justify-center bg-gradient-to-l from-gray-200 md:bg-none">
      <h1 class="text-3xl font-bold md:mb-4 md:text-4xl lg:text-6xl">בית החיות קריות</h1>
      <h2 class="text-lg font-bold md:mb-4 lg:text-3xl">מזמינים מבלי לצאת מהבית</h2>
      <div class="max-w-sm mb-8 text-md font-light lg:max-w-md text-balance">
        <p>מהיום כל המצרכים לחיית מחמד שלכם נמצאים במקום אחד ובמרחק קליקים בודדים, מזמינים מהאתר ומקבלים משלוח עד הבית</p>
      </div>
      <NuxtLink class="px-6 py-3 font-bold text-white bg-gray-800 rounded-xl hover:bg-gray-800" to="/products">נשמע מיאו!</NuxtLink>
    </div>
  </div>
</template>
