# cuzzy

// ==UserScript==
// @name         Autofill Gmail Signup Form
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Autofill Gmail signup form
// @author       You
// @match        https://accounts.google.com/signup*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';
    
    // Cek jika halaman pendaftaran Gmail sudah dimuat
    if (document.querySelector('input[type="text"]') && document.querySelector('input[type="password"]')) {
        // Mengisi nama depan dan belakang
        document.querySelector('input[name="firstName"]').value = 'John';
        document.querySelector('input[name="lastName"]').value = 'Doe';
        
        // Mengisi alamat email
        document.querySelector('input[name="Username"]').value = 'johndoe12345';
        
        // Mengisi password dan konfirmasi password
        document.querySelector('input[name="Passwd"]').value = 'SecurePassword123';
        document.querySelector('input[name="ConfirmPasswd"]').value = 'SecurePassword123';
    }
})();
