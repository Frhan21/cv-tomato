<template>
  <div class="h-[1000px] flex justify-center items-center flex-col">
    <div class="flex justify-center items-center flex-col mb-10">
      <p class="font-semibold text-[1.5rem] mb-0 mt-10 uppercase">Meet</p>
      <h2 class="text-[2.5rem] font-bold">Our Teams</h2>
    </div>
    <Card
      nama="Drs.Harmadi, M.Si"
      jurusan="Dosen Universitas Andalas"
      jabatan="Dosen Pembimbing"
      imgSrc="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYrF8MdL-hasz7_gNW2f_7Y8EmKJ5fwsPR94ZxtlrE&s"
    />
    <div class="flex justify-center mt-10">
      <Card
        nama="Muhammad Rido Isdi"
        jurusan="Fisika (2019)"
        jabatan="Ketua Tim"
        imgSrc="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8Q42_1jDiESjrU16Y9RdMakMZDyPJkGyM5zz2Jht5&s"
      />
    </div>
    <div class="flex flex-wrap mt-5 gap-6">
      <Card
        v-for="item in profileArry"
        :key="item.id"
        :nama="item.nama"
        :jurusan="item.jurusan"
        :jabatan="item.jabatan"
      />
    </div>
  </div>
</template>

<script>
import Card from "../components/Card.vue"
export default {
  components: { Card },
  data() {
    return {
      profileArry: [
        {
          id: 1,
          nama: "Abi Syaibah",
          jurusan: "Fisika (2020)",
          jabatan: "Anggota 1",
        },
        {
          id: 2,
          nama: "Tuti Alawiyah",
          jurusan: "Fisika (2020)",
          jabatan: "Anggota 2",
        },
        {
          id: 3,
          nama: "M Farhan Ramadhan",
          jurusan: "Fisika (2020)",
          jabatan: "Anggota 3",
        },
      ],
    }
  },
}
</script>
