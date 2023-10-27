<template>
    <div class="flex flex-col px-56 text-white space-y-2 mb-8" id="contact">
        <h1 class="text-2xl font-semibold">
            Benimle İletişime Geçin
        </h1>
        <form class="flex flex-col space-y-4">
            <label for="email">
                E-Postanız
            </label>
            <input type="email" id="email"/>
            <label for="phone">
                Telefon Numaranız
            </label>
            <input type="tel" id="phone"/>
            <label for="content">
                Mesajınız
            </label>
            <textarea class="min-h-[120px]" id="content"/>

            <button class="bg-green-500 w-1/4 mx-auto rounded-lg px-4 py-2 hover:bg-green-600">
                Gönder
            </button>
        </form>

    </div>
</template>

<style scoped>
input,
textarea {
    padding-top: 0.35rem;
    padding-bottom: 0.35rem;
    padding-left: 1rem;
    padding-right: 1rem;
    border-radius: 0.25rem;
    border-width: 1px;
    border-color: #39475c;
    background-color: #39475c;
    transition: all 0.2s ease-in-out;
}

input:focus,
textarea:focus {
    outline: 0.5px solid transparent;
    outline-offset: 0.5px;
    border-color: #6b6de6;
    box-shadow: 0 0 0 3px rgb(95, 88, 221);
}
</style>