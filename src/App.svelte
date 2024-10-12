<script>
  import "./app.css";
  import "@fontsource/delius-swash-caps";

  let nama = "";
  const urlParams = new URLSearchParams(window.location.search);
  $: nama = urlParams.get("to") || "";

  function hitungMundur() {
    const tanggalTujuan = new Date("2024-10-19T15:00:00+07:00").getTime();
    const sekarang = new Date().getTime();
    const selisih = tanggalTujuan - sekarang;

    const hari = Math.floor(selisih / (1000 * 60 * 60 * 24));
    const jam = Math.floor(
      (selisih % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
    );
    const menit = Math.floor((selisih % (1000 * 60 * 60)) / (1000 * 60));
    const detik = Math.floor((selisih % (1000 * 60)) / 1000);

    return { hari, jam, menit, detik };
  }
  let { hari, jam, menit, detik } = hitungMundur();
  setInterval(() => {
    ({ hari, jam, menit, detik } = hitungMundur());
  }, 1000);

  import { onMount } from "svelte";

  let audioPlayer;

  onMount(() => {
    audioPlayer = new Audio("backsound-AQIQAH-DIGITAL-1.mp3");
    audioPlayer.loop = true;
    audioPlayer.play();
  });

  function toggleMusic() {
    if (audioPlayer.paused) {
      audioPlayer.play();
    } else {
      audioPlayer.pause();
    }
  }
</script>

<svelte:head>
  <title>Tasyakuran Aqiqah Saddam Manaf Hasyim</title>
  <meta property="og:title" content="Tasyakuran Aqiqah" />
  <meta
    property="og:image"
    content="7933ab41-013a-41ea-80b3-a198972da5a3.jpeg"
  />
  <meta
    property="og:description"
    content="Undangan Tasyakuran Aqiqah Saddam Manaf Hasyim"
  />
  <meta
    name="description"
    content="Undangan Tasyakuran Aqiqah Saddam Manaf Hasyim"
  />
</svelte:head>
<center>
  <main class="min-h-screen">
    <div class="fixed bottom-4 left-4 z-50">
      <button
        on:click={toggleMusic}
        class="bg-[#79c7a1] text-white px-4 py-2 rounded-full shadow-lg"
      >
        {#if audioPlayer && !audioPlayer.paused}
          Pause
        {:else}
          Play
        {/if}
      </button>
    </div>
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
            src="7933ab41-013a-41ea-80b3-a198972da5a3.jpeg"
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
        <h1>Sabtu, 19 Oktober 2024</h1>
        <div class="grid grid-cols-4 gap-4 mb-8 mt-8">
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">{hari}</span>
            <span class="text-sm">Hari</span>
          </div>
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">{jam}</span>
            <span class="text-sm">Jam</span>
          </div>
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">{menit}</span>
            <span class="text-sm">Menit</span>
          </div>
          <div
            class="bg-white rounded-lg shadow-md p-4 flex flex-col items-center"
          >
            <span class="text-xl font-bold mb-1">{detik}</span>
            <span class="text-sm">Detik</span>
          </div>
        </div>

        <div class="mb-8 text-center flex flex-col gap-4">
          <h2 class="text-xl font-bold mb-4">Tamu Undangan</h2>
          <div
            class="bg-white rounded-lg shadow-xl p-6 border border-gray-200 hover:shadow-2xl transition-shadow duration-300 flex flex-col gap-2"
          >
            <p class="mb-2 text-gray-600">Kepada Yth.</p>
            <h3 class="text-xl font-bold mb-2">{nama}</h3>
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
            <p class="text-md mt-10">
              Dengan segala kerendahan hati kami berharap kehadiran
              Bapak/Ibu/Saudara/i dalam acara Tasyakuran Aqiqah anak kami yang
              akan diselenggarakan pada :
            </p>
            <div class="flex justify-center mt-6">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="w-12 h-12 text-[#79c7a1] animate-bounce"
              >
                <path
                  fill-rule="evenodd"
                  d="M6.75 2.25A.75.75 0 017.5 3v1.5h9V3A.75.75 0 0118 3v1.5h.75a3 3 0 013 3v11.25a3 3 0 01-3 3H5.25a3 3 0 01-3-3V7.5a3 3 0 013-3H6V3a.75.75 0 01.75-.75zm13.5 9a1.5 1.5 0 00-1.5-1.5H5.25a1.5 1.5 0 00-1.5 1.5v7.5a1.5 1.5 0 001.5 1.5h13.5a1.5 1.5 0 001.5-1.5v-7.5z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <div class="mt-4">
              <p class="text-md font-delius">
                <strong>Hari/Tanggal:</strong> Sabtu, 19 Oktober 2024
              </p>
              <p class="text-md mt-2 font-delius">
                <strong>Waktu:</strong> 15.00 WIB - Selesai
              </p>
              <p class="text-md mt-2 font-delius">
                <strong>Tempat:</strong> TAMAN CIPTA ASRI BLOK MANGO NO 26<br />
              </p>
            </div>
          </div>
        </div>

        <div class="mb-8 text-center w-full">
          <div class="border-2 border-[#79c7a1] rounded-lg p-6 shadow-2xl">
            <h1 class="text-2xl font-bold font-delius text-amber-800">
              Galeri
            </h1>
            <div class="grid grid-cols-2 gap-4 mt-6">
              <div>
                <img
                  src="5131c67b-0ac9-4be8-a4f0-48f130134240.jpeg"
                  alt="Gambar 4"
                  class="w-full h-auto rounded-lg"
                />
              </div>
              <div>
                <img
                  src="219edac2-1d61-438d-a6d5-9d1dd6accf19.jpeg"
                  alt="Gambar 2"
                  class="w-full h-auto rounded-lg"
                />
              </div>
              <div>
                <img
                  src="354ee1d7-028b-491c-9279-bd6ab52879fe.jpeg"
                  alt="Gambar 3"
                  class="w-full h-auto rounded-lg"
                />
              </div>
              <div>
                <img
                  src="7933ab41-013a-41ea-80b3-a198972da5a3.jpeg"
                  alt="Gambar 1"
                  class="w-full h-auto rounded-lg"
                />
              </div>
            </div>
          </div>
        </div>

        <div
          style="background-image: url('bg.png'); background-size: cover; background-repeat: repeat; background-position: center;"
          class="text-center py-8 w-full"
        >
          <div class="flex justify-center gap-4">
            <img src="2-12-e1677209532589.webp" alt="" />
            <img src="2-12-e1677209532589.webp" alt="" />
          </div>
          <div class="relative flex justify-center mb-12">
            <div
              class="rounded-full w-72 h-72 flex items-center justify-center mb-2 absolute"
            >
              <img
                src="awan.webp"
                alt="Awan"
                class="h-20 w-20 left-0 absolute"
              />
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
              src="7933ab41-013a-41ea-80b3-a198972da5a3.jpeg"
              alt="Foto Aqiqah"
              class="w-48 h-48 object-cover rounded-full mx-auto"
            />
          </div>
          <div class="text-center flex flex-col items-center gap-4">
            <h1 class="text-2xl font-bold mb-2 font-delius">
              Saddam Manaf Hasyim. F
            </h1>
          </div>
          <p class="text-md font-delius text-slate-800 mt-4">
            Kami Yang Berbahagia Keluarga Besar
          </p>
          <h1 class="text-2xl font-delius">Bpk. Rio & Ibu Ririn</h1>
          <p class="text-md font-delius text-slate-800 mt-4">
            Atas kehadiran dan doa restunya kami ucapkan terima kasih
          </p>
          <p class="text-md font-delius text-slate-800 mt-4">
            Wassalamu’alaikum Wr. Wb.
          </p>
        </div>
        <div class="flex justify-center gap-4">
          <img src="2-12-e1677209532589.webp" alt="" />
          <img src="2-12-e1677209532589.webp" alt="" />
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
