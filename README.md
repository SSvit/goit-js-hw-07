# goit-js-hw-07

    Завдання 1 - галерея зображень
1. Створи галерею з можливістю кліку по її елементах і перегляду повнорозмірного зображення у модальному вікні. 
2. Подивися демо відео роботи галереї.
3. Виконуй це завдання у файлах 01-gallery.html і 01-gallery.js. Розбий його на декілька підзавдань:

1) Створення і рендер розмітки на підставі масиву даних galleryItems і наданого шаблону елемента галереї.
Реалізація делегування на div.gallery і отримання url великого зображення.
Підключення скрипту і стилів бібліотеки модального вікна basicLightbox. Використовуй CDN сервіс jsdelivr і додай у проект посилання на мініфіковані (.min) файли бібліотеки.
Відкриття модального вікна по кліку на елементі галереї. Для цього ознайомся з документацією і прикладами.
Заміна значення атрибута src елемента <img> в модальному вікні перед відкриттям. Використовуй готову розмітку модального вікна із зображенням з прикладів бібліотеки basicLightbox.



// document.querySelector("button.image").onclink = () => {
//     basicLightbox
//     .create(
//         `
//         <img width  = "1400" src = 'https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677__340.jpg'/>
//         `
//     )
//     .show();
// };



Варіант 2

// import { galleryItems } from "./gallery-items.js";

// // Change code below this line

// const galleryList = document.querySelector(".gallery");




// const galleryItemsMarkup = galleryItems

//   .map(

//     (img) =>

//       `<div class="gallery__item">

//       <a class="gallery__link" href=${img.original}>

//       <img

//       class="gallery__image"

//       src=${img.preview}

//       data-source=${img.original}

//       alt=${img.description}

//     />

//     </a>

//     </div>`

//   )

//   .join("");

// galleryList.insertAdjacentHTML("afterbegin", galleryItemsMarkup);




// galleryList.addEventListener("click", getModalImg);




// function getModalImg(evt) {

//   evt.preventDefault();




//   if (evt.target.nodeName !== "IMG") {

//     return;

//   }

//   const modalImg = basicLightbox.create(`

//   <img src="${evt.target.dataset.source}">

// `);

//   modalImg.show();




//   galleryList.addEventListener("keydown", (evt) => {

//     if (evt.code === "Escape") {

//       modalImg.close();

//     }

//   });

// }