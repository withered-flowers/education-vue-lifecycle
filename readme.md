## Table of Content
1. [JSON Server](#json-server)
1. [Vue Lifecycle](#vue-lifecycle)
    - [Lifecycle Breakdown](#lifecycle-breakdown)
      - created
      - mounted
      - updated
      - destroyed
    - Which Lifecycle?
      - fetchData
      - checkToken
1. Mari Demo !
1. Computed & Watched
1. [Referensi](#referensi)

## JSON Server

## Vue Lifecycle
VueJS ini adalah sebuah Frontend framework pada javascript yang menggunakan Virtual DOM.  
Mirip pada DOM yang memiliki event siklus onready, onsubmit dan sebagainya, di VueJS ini  
pun memiliki beberapa siklus event yang disediakan di dalam VueJS ini.

Untuk melihat keseluruhan diagram siklus kehidupan dari instance pada VueJS, bisa dilirik  
di sini yah https://vuejs.org/v2/guide/instance.html#Lifecycle-Diagram

TL;DR  
Mirip hooks yang ada di sequelize.

### Lifecycle Breakdown
Mari kita lihat satu per satu lifecycle event yang ada di VueJS ini yah !

#### created
Nama lifecycle hook: **beforeCreate** & **created**  

Pada lifecycle ini, bisa mengakses data reaktif dan event yang ada, tapi template tampilan belum  
ada.

**Paling sering digunakan**

#### mounted
Nama lifecycle hook: **beforeMount** & **mounted**

Pada lifecycle ini, bisa / memiliki akses penuh terhadap komponen reaktif, templates, dan DOM   
yang sudah dirender.

Gunakan ini apabila kita membutuhkan akses atau memodifikasi DOM pada komponen secepatnya, sebelum 
atau sesudah render awal (initial render).

#### updated
Nama lifecycle hook: **beforeUpdate** & **updated**
(Tidak dicontohkan)

Lifecycle ini dipanggil ketika ada data yang berubah dan menyebabkan virtual DOM nya di render  
ulang dan ditambalsulam.

Cocok digunakan untuk menghapus event listener secara manual (untuk optimasi)

#### destroyed
Nama lifecycle hook: **beforeDestroy** & **destroyed**

Lifecycle ini dipanggil ketika instance vue sudah akan atau telah di destroy.

### Mari Demo
- Demo JSON-Server
- Axios

#### Step by step (Part 1)
1. Handle Login
1. Add Axios to fetch data from mock server
1. Add SweetAlert Script for error handling
1. Created or Mounted?
1. Check token exist
1. Fetch data todos
1. Logout (LocalStorage Strategy)
1. Add Logic for Add ToDo
1. Add ToDo with Re-Fetch
1. id already auto-increment, so?
1. Delete with axios
1. Second Strategy (Delete without refetch)


### Computed & Watch
Computed -> Complex Logic (Olah data)
Watch -> Melihat ada perubahan data

#### Step by step (Part 2)
1. Add Checkbox for Filter All / Done / Not Done
1. Add todosFilter
1. Computed for todos, filter by filterName

## Referensi
* https://vuejs.org/v2/api/
* https://vuejs.org/v2/guide/instance.html#Lifecycle-Diagram
* https://medium.com/badr-interactive/mengenal-lifecycle-hooks-pada-vue-js-78cd2225a69
* https://www.digitalocean.com/community/tutorials/vuejs-component-lifecycle