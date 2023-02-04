<template>
  <div class="h-screen colorBg">
    <div class="grid grid-rows-2 gap-none">

      <div class="col-span-4 flex items-center justify-center">
        <span class="titlePage font-bold text-3xl">Scan your QR Code</span>
      </div>

      <div class="col-span-4 flex items-center justify-center">
        <img class="w-64" src="~/assets/image.png" alt="image" />
      </div>

      <div class="col-span-4 flex items-center justify-center">
          <NavBottom> </NavBottom>
      </div>

    </div>

  </div>

</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

.titlePage {
  font-family: 'Poppins', sans-serif;
}

.colorBg {
  background-color: #F4FDFF;
}
</style>
