---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS (experimental)
css: unocss
---

# Welcome to Slidev

Presentation slides for developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---

# Animation Examples

Let's explore some engaging animations!

<div class="grid grid-cols-2 gap-4">
<div class="space-y-4">

## Slide In
<AnimatedBox 
  :initial="{ x: -100, opacity: 0 }" 
  :enter="{ x: 0, opacity: 1, transition: { duration: 1000 } }" 
/>

## Fade Up
<AnimatedText 
  text="Hello Slidev!" 
  :initial="{ y: 100, opacity: 0 }" 
  :enter="{ y: 0, opacity: 1, transition: { delay: 300 } }" 
/>

</div>
<div class="space-y-4">

## Scale
<AnimatedBox 
  :initial="{ scale: 0 }" 
  :enter="{ scale: 1, transition: { type: 'spring', stiffness: 300, damping: 20 } }" 
/>

## Rotate
<AnimatedBox 
  :initial="{ rotate: 180, scale: 0 }" 
  :enter="{ rotate: 0, scale: 1, transition: { duration: 1000 } }" 
/>

</div>
</div>

---

# Combining Animations

Create complex animations by combining multiple properties

<div class="grid grid-cols-3 gap-8 items-center">
  <AnimatedBox 
    :initial="{ x: -100, y: 100, rotate: 45, opacity: 0 }" 
    :enter="{ 
      x: 0, 
      y: 0, 
      rotate: 0, 
      opacity: 1, 
      transition: { duration: 1000 } 
    }" 
  />

  <AnimatedText 
    text="Smooth Transitions" 
    :initial="{ scale: 0.5, opacity: 0 }" 
    :enter="{ 
      scale: 1, 
      opacity: 1, 
      transition: { delay: 500, duration: 800 } 
    }" 
  />

  <AnimatedBox 
    :initial="{ scale: 2, opacity: 0 }" 
    :enter="{ 
      scale: 1, 
      opacity: 1, 
      transition: { type: 'spring', stiffness: 200 } 
    }" 
  />
</div>

<div class="mt-12">
  <AnimatedText 
    text="Animations make your presentations more engaging!" 
    :initial="{ y: 50, opacity: 0 }" 
    :enter="{ 
      y: 0, 
      opacity: 1, 
      transition: { delay: 1000, duration: 1000 } 
    }" 
  />
</div>

---

# Interactive Animations

Hover and click interactions

<div class="grid grid-cols-2 gap-8">
  <div
    v-motion
    :initial="{ scale: 1 }"
    :hover="{ scale: 1.1 }"
    :tap="{ scale: 0.95 }"
    class="p-8 bg-blue-500 rounded-lg cursor-pointer text-white text-center"
  >
    Hover and Click Me!
  </div>

  <div
    v-motion
    :initial="{ rotate: 0 }"
    :hover="{ rotate: 180 }"
    class="p-8 bg-green-500 rounded-lg cursor-pointer text-white text-center"
  >
    Hover to Rotate
  </div>
</div>

<style>
.slidev-layout {
  background-color: #ffffff;
  background-image: linear-gradient(180deg, #ffffff 0%, #f3f4f6 100%);
}
</style>

<!-- Rest of the original slides content remains unchanged -->