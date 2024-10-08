<script>
  import "./app.css";
  import "@fontsource/delius-swash-caps";
</script>

<center>
  <main class="min-h-screen">
    <div
      class="w-full h-screen px-4 pt-5"
      style="background-image: url('bg.png'); background-size: cover; background-repeat: repeat; background-position: center;"
    >
      <div
        class=" px-2 pt-4 w-full max-w-xl items-center justify-center flex flex-col"
      >
        <div class="relative flex justify-center mb-12">
          <div
            class="rounded-full w-72 h-72 flex items-center justify-center mb-2 absolute"
          >
            <img src="awan.webp" alt="Awan" class="h-20 w-20 left-0 absolute" />
            <svg viewBox="0 0 100 100" class="absolute inset-0">
              <defs>
                <path
                  id="circle"
                  d="M 50, 50 m -37, 0 a 37,37 0 1,1 74,0 a 37,37 0 1,1 -74,0"
                />
              </defs>
              <text font-size="10" text-anchor="middle" class="font-delius">
                <textPath xlink:href="#circle" startOffset="25%">
                  Tasyakuran Aqiqah
                </textPath>
              </text>
            </svg>
          </div>
        </div>

        <div class="mb-4">
          <img
            src="profile.jpeg"
            alt="Foto Aqiqah"
            class="w-48 h-48 object-cover rounded-full mx-auto"
          />
        </div>
        <div class="text-center flex flex-col items-center gap-4">
          <h1 class="text-2xl font-bold mb-2 font-delius">
            Saddam Manaf Hasyim. F
          </h1>
          <p class="text-lg mb-4 text-center">
            Putra dari Bapak Rio Denny Fatresa
            <br />
            &
            <br />
            Ibu Ririn Meiriza
          </p>
        </div>

        <div class="grid grid-cols-4 gap-4 mb-8 mt-8">
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">00</span>
            <span class="text-sm">Hari</span>
          </div>
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">00</span>
            <span class="text-sm">Jam</span>
          </div>
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">00</span>
            <span class="text-sm">Menit</span>
          </div>
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">00</span>
            <span class="text-sm">Detik</span>
          </div>
        </div>

        <div class="mb-8 text-center flex flex-col gap-4">
          <h2 class="text-xl font-bold mb-4">Tamu Undangan</h2>
          <div
            class="bg-white rounded-lg shadow-xl p-6 border border-gray-200 hover:shadow-2xl transition-shadow duration-300 flex flex-col gap-2"
          >
            <p class="mb-2 text-gray-600">Kepada Yth.</p>
            <h3 class="text-xl font-bold mb-2">Keluarga Bapak Hasyim</h3>
            <p class="text-xs">
              Tanpa mengurangi rasa hormat, kami mengundang Anda untuk berhadir
              di acara Tasyakuran Aqiqah putra kami.
            </p>
          </div>
        </div>

        <div class="mb-8 text-center w-full">
          <div class="border-2 border-[#79c7a1] rounded-lg p-6 shadow-2xl">
            <div class="flex flex-row justify-between gap-2">
              <img
                src="Upload-yg-ini-1-e1677135394670-1.webp"
                class="w-20"
                alt=""
              />
              <img src="Upload-yg-ini.webp" class="w-20" alt="" />
            </div>
            <h1 class="text-2xl font-bold font-delius text-amber-800">
              Al-Isra’ ayat 24
            </h1>
            <p class="text-xl mt-10">
              " Dan hendaknya rendahkanlah dirimu terhadap mereka berdua dengan
              penuh kesayangan lalu ucapkanlah: “Wahai Tuhanku, kasihilah mereka
              keduanya, sebagaimana mereka berdua (orang tua)telah mendidikku
              waktu kecil ”.
            </p>
          </div>
        </div>

        <div class="mb-8 text-center w-full">
          <div class="border-2 border-[#79c7a1] rounded-lg p-6 shadow-2xl">
            <h1 class="text-2xl font-bold font-delius text-amber-800">Acara</h1>
            <p class="text-xl mt-10">
              " Dan hendaknya rendahkanlah dirimu terhadap mereka berdua dengan
              penuh kesayangan lalu ucapkanlah: “Wahai Tuhanku, kasihilah mereka
              keduanya, sebagaimana mereka berdua (orang tua)telah mendidikku
              waktu kecil ”.
            </p>
          </div>
        </div>
      </div>
    </div>
  </main>
</center>

<style>
  .font-delius {
    font-family: "Delius Swash Caps", cursive;
  }
</style>
