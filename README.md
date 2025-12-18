<!DOCTYPE html>
<html lang="ur">
<head>
    <meta charset="UTF-8">
    <title>Copying Notes...</title>
    <style>
        body { font-family: sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background-color: #fdfaf5; }
        .status { padding: 20px; border-radius: 10px; background: white; border: 2px solid #8b0000; text-align: center; }
    </style>
</head>
<body>

<div class="status">
    <h3 id="msg">Copying Notes...</h3>
    <p>Please wait a moment.</p>
</div>

<div id="notesData" style="display: none;">
(1) Fiqh ki Tareef aur Mauzu
Fiqh ka ma'ana Lughvi Taur Par kisi cheez ki samjh boojh hasil karna, Cheezon Ko Achi Tarah se gehrai se samajhna ye hei Fiqh.

Istilahı Tareef: Quran-o-Hadees, Ijma, aur Qiyaas ke mutabiq, Shariat Ke Amali Ahkamat Ko Tafseeli Daleelo se maloom karna.

Amali Ahkaamat: Ye shariyat ke Ahkamat hai medical science ke Ahkamat nahi hai. Jinka talluq Aqeede ya Akhlaq se nahi hai, balki Aapke Amali Ahkaamat Jaise Namaaz, Roza, Taharat in chizo ko maloom karna dalil ke Saath.
"Iqra (اقرأ)" (padho) iss baat ki dalil hai ke islam sirf ilm ke saath chala jaa sakta hai.

(2) Fiqh ke do Bade Topic:
(i) Ibadat: Taharat, Namaz, Roza, Zakaat, Hajj, Jihad.
(ii) Muamalat: Khareedo-frokht, Tijarat, Nikah-Talaq aur Haram-o-Halal ke masail.

3. Ikhtilaf ka hal:-
(1) Ikhtilaf ka maujood hona: Musalmano ke darmiyan ye ikhtilafat bahut purane hai aur Allah ki taraf se ek Aazmaish hai. Allah chahta to sabhi ko hidayat deta, lekin ye duniya imtihan hai.

(2) Ikhtilafaat me kya farz hai:
Agar tanaza ho jaye to usko Allah (Quran) Aur uske rasool (Sunnat) ki taraf lotao. Agar tum Allah aur Aakhirat par imaan rakhte ho, to hal Quran aur Hadees se lo.

Allah farmata hai ke Nabi (S.A.W) apni marzi se baat nahi karte, wo Allah ki taraf se hoti hai. Har sunnat par amal karna chaho chahe koi bhi rasta ho.

Aimma-e-Kiraam:
1. Imam Abu Hanifa (R.A): (80 Hijri - 150 Hijri)
2. Imam Malik (R.A): (93 Hijri - 179 Hijri)
3. Imam Shafi (R.A): (150 Hijri - 204 Hijri)
4. Imam Ahmed bin Hanbal (R.A): (164 Hijri - 241 Hijri)
</div>

<script>
    window.onload = function() {
        const textToCopy = document.getElementById('notesData').innerText;
        const msgElement = document.getElementById('msg');

        navigator.clipboard.writeText(textToCopy).then(() => {
            msgElement.innerText = "Notes Copied! ✅";
            msgElement.style.color = "green";
            // Optional: Close window or redirect after 2 seconds
            setTimeout(() => { window.history.back(); }, 1500);
        }).catch(err => {
            msgElement.innerText = "Error copying. Please try again.";
            msgElement.style.color = "red";
        });
    }
</script>

</body>
</html>
