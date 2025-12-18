<!DOCTYPE html>
<html lang="ur">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Copy Notes</title>
    <style>
        body { font-family: sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background-color: #fdfaf5; }
        .box { padding: 30px; border-radius: 15px; background: white; border: 2px solid #8b0000; text-align: center; box-shadow: 0 4px 10px rgba(0,0,0,0.1); width: 80%; }
        .btn { background-color: #8b0000; color: white; border: none; padding: 15px 25px; border-radius: 8px; font-size: 18px; font-weight: bold; cursor: pointer; margin-top: 15px; width: 100%; }
        .btn:active { background-color: #5d0000; }
        #status { margin-top: 15px; font-weight: bold; }
    </style>
</head>
<body>

<div class="box">
    <h2 style="color: #8b0000; margin: 0;">Fiqh Notes</h2>
    <p>Niche diye gaye button par click karke notes copy karein.</p>
    
    <button class="btn" onclick="copyNow()">Click to Copy Notes</button>
    
    <div id="status"></div>
</div>

<div id="notesText" style="display: none;">
(1) Fiqh ki Tareef aur Mauzu:
Fiqh ka ma'ana Lughvi Taur Par kisi cheez ki samjh boojh hasil karna. Istilahi Tareef: Quran-o-Hadees, Ijma, aur Qiyaas ke mutabiq, Shariat Ke Amali Ahkamat Ko Tafseeli Daleelo se maloom karna.

(2) Fiqh ke do Bade Topic:
(i) Ibadat: Taharat, Namaz, Roza, Zakaat, Hajj, Jihad.
(ii) Muamalat: Khareedo-frokht, Tijarat, Nikah-Talaq aur Haram-o-Halal ke roz-marra ke masail.

(3) Ikhtilaf ka hal:
Musalmano ke darmiyan aksar masail mein ikhtilafat paaye jaate hain jo Allah ki taraf se ek aazmaish hai. Agar tumhara ikhtilaf ho jaye to usko Allah (Quran) aur uske rasool (Sunnat) ki taraf lotao.

Aimma-e-Kiraam:
1. Imam Abu Hanifa (R.A)
2. Imam Malik (R.A)
3. Imam Shafi (R.A)
4. Imam Ahmed bin Hanbal (R.A)
</div>

<script>
    function copyNow() {
        const text = document.getElementById('notesText').innerText;
        const status = document.getElementById('status');
        
        navigator.clipboard.writeText(text).then(() => {
            status.innerText = "Notes Copied! ✅";
            status.style.color = "green";
            // 2 second baad wapas Canva par jane ke liye
            setTimeout(() => { window.history.back(); }, 2000);
        }).catch(err => {
            status.innerText = "Error! Please try again.";
            status.style.color = "red";
        });
    }
</script>

</body>
</html>
