<!DOCTYPE html>
<html>
<head>
<style>
  body { background-color: transparent; margin: 0; padding: 10px; }
  .notes-card {
    font-family: 'Segoe UI', Arial, sans-serif;
    background-color: #1a1a1a; /* Dark background like your screenshot */
    color: #ffffff;
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  }
  .header-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #444;
    padding-bottom: 10px;
    margin-bottom: 15px;
  }
  .copy-btn {
    background-color: #8b0000;
    color: white;
    border: none;
    padding: 8px 16px;
    border-radius: 6px;
    cursor: pointer;
    font-weight: bold;
    transition: 0.3s;
  }
  .copy-btn:hover { background-color: #a00000; }
  .content { line-height: 1.6; white-space: pre-wrap; font-size: 15px; }
  .heading { color: #ffd700; font-size: 18px; font-weight: bold; margin-bottom: 5px; }
</style>
</head>
<body>

<div class="notes-card">
  <div class="header-row">
    <span style="color: #ffd700; font-weight: bold;">Class 00: Fiqh Notes</span>
    <button class="copy-btn" onclick="copyNotes()">Copy Text</button>
  </div>
  
  <div class="content" id="myNotes">
(1) Fiqh ki Tareef aur Mauzu
Fiqh kya hai?
Fiqh ka ma'ana Lughvi Taur Par kisi cheez ki samjh boojh hasil karna, Cheezon Ko Achi Tarah se gehrai se samajhna ye hei Fiqh.

Istilahı Tareef:
Quran-o-Hadees, Ijma, aur Qiyaas ke mutabiq, Shariat Ke Amali Ahkamat Ko Tafseeli Daleelo se maloom karna.

Amali Ahkaamat: Ye shariyat ke Ahkamat hai medical science ke Ahkamat nahi hai, aur Amali Ahkaamat hai jiska talluq Aqeede se nahi hai, Jinka talluq Akhlaq se nahi hai, balki Aapke Amali Ahkaamat Jaise Namaaz, Roza, Taharat in chizo ko maloom karna dalil ke Saath.

Quran ka sabse pehla lafz jo nazil hua wo tha "iqra (اقرأ)" (padho), jo iss baat ki dalil hai ke islam wo deen hai jo sirf ilm ke saath chala jaa sakta hai .

(2) Fiqh ke do Bade Topic:
(i) Ibadat: Taharat, Namaz, Roza, Zakaat, Hajj, Jihad.
(ii) Muamalat: Khareedo-frokht, Tijarat, Nikah-Talaq aur Haram-o-Halal ke roz-marra ke masail.
  </div>
</div>

<script>
function copyNotes() {
  const text = document.getElementById('myNotes').innerText;
  navigator.clipboard.writeText(text).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.innerText = "Copied! ✅";
    btn.style.backgroundColor = "#28a745";
    setTimeout(() => {
      btn.innerText = "Copy Text";
      btn.style.backgroundColor = "#8b0000";
    }, 2000);
  });
}
</script>

</body>
</html>
