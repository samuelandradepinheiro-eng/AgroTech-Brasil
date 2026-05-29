// ===============================
// MENU MOBILE
// ===============================

const menuBtn = document.querySelector(".menu-btn");
const navMenu = document.querySelector(".nav-links");

menuBtn.addEventListener("click", () => {
    navMenu.classList.toggle("active");
});


// ===============================
// HEADER EFEITO AO ROLAR
// ===============================

const navbar = document.querySelector("nav");

window.addEventListener("scroll", () => {

    if(window.scrollY > 100){
        navbar.classList.add("scroll-nav");
    } else {
        navbar.classList.remove("scroll-nav");
    }

});


// ===============================
// TEXTO DIGITANDO
// ===============================

const textArray = [
    "O Agro Move o Brasil",
    "Tecnologia no Campo",
    "Produção com Sustentabilidade",
    "Força que Alimenta o Mundo"
];

let typingText = document.querySelector(".typing-text");

let arrayIndex = 0;
let charIndex = 0;

function typeEffect(){

    if(charIndex < textArray[arrayIndex].length){

        typingText.textContent += textArray[arrayIndex].charAt(charIndex);

        charIndex++;

        setTimeout(typeEffect, 100);

    } else {

        setTimeout(eraseEffect, 2000);

    }

}

function eraseEffect(){

    if(charIndex > 0){

        typingText.textContent = textArray[arrayIndex].substring(0, charIndex - 1);

        charIndex--;

        setTimeout(eraseEffect, 50);

    } else {

        arrayIndex++;

        if(arrayIndex >= textArray.length){
            arrayIndex = 0;
        }

        setTimeout(typeEffect, 500);

    }

}

document.addEventListener("DOMContentLoaded", () => {

    if(textArray.length){
        setTimeout(typeEffect, 1000);
    }

});


// ===============================
// CONTADOR ANIMADO
// ===============================

const counters = document.querySelectorAll(".counter");

counters.forEach(counter => {

    counter.innerText = "0";

    const updateCounter = () => {

        const target = +counter.getAttribute("data-target");

        const current = +counter.innerText;

        const increment = target / 100;

        if(current < target){

            counter.innerText = `${Math.ceil(current + increment)}`;

            setTimeout(updateCounter, 30);

        } else {

            counter.innerText = target;

        }

    };

    updateCounter();

});


// ===============================
// SCROLL SUAVE
// ===============================

document.querySelectorAll('a[href^="#"]').forEach(anchor => {

    anchor.addEventListener("click", function(e){

        e.preventDefault();

        const target = document.querySelector(this.getAttribute("href"));

        target.scrollIntoView({
            behavior: "smooth"
        });

    });

});


// ===============================
// ANIMAÇÃO AO APARECER
// ===============================

const revealElements = document.querySelectorAll(".reveal");

window.addEventListener("scroll", revealScroll);

function revealScroll(){

    for(let i = 0; i < revealElements.length; i++){

        let windowHeight = window.innerHeight;

        let revealTop = revealElements[i].getBoundingClientRect().top;

        let revealPoint = 100;

        if(revealTop < windowHeight - revealPoint){

            revealElements[i].classList.add("active");

        }

    }

}


// ===============================
// BOTÃO VOLTAR AO TOPO
// ===============================

const topBtn = document.querySelector(".top-btn");

window.addEventListener("scroll", () => {

    if(window.scrollY > 400){

        topBtn.classList.add("show");

    } else {

        topBtn.classList.remove("show");

    }

});

topBtn.addEventListener("click", () => {

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });

});


// ===============================
// FORMULÁRIO
// ===============================

const form = document.querySelector("#contact-form");

form.addEventListener("submit", (e) => {

    e.preventDefault();

    let nome = document.querySelector("#nome").value;
    let email = document.querySelector("#email").value;

    if(nome === "" || email === ""){

        alert("Preencha todos os campos!");

    } else {

        alert("Mensagem enviada com sucesso!");

        form.reset();

    }

});


// ===============================
// DARK MODE
// ===============================

const darkBtn = document.querySelector(".dark-mode-btn");

darkBtn.addEventListener("click", () => {

    document.body.classList.toggle("dark-mode");

});
