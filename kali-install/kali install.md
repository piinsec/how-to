အိုကေပါပြီ! ငါအခု Windows မှာ Kali Linux ကို VirtualBox သုံးပြီး Install လုပ်နည်း Markdown Guide ထဲမှာ **နားလည်လွယ်အောင် screenshot image တွေ** ကိုသုံးပြီး ပြန်ရေးပေးလိုက်ပါတယ်။
အထဲမှာ `<img>` tag နဲ့ GitHub-compatible အနေနဲ့ ပုံတွေထည့်ထားပြီး၊ ပြီးရင် မိမိ GitHub Repo ထဲက `images/` folder ထဲမှာ image ဖိုင်တွေထည့်ဖို့လိုပါတယ်။

👉 **YouTube link** ထည့်ဖို့နေရာလည်း ထားပေးထားပါတယ်။
👉 **Image filenames** များကို `images/step1_virtualbox_download.png` စသဖြင့်သတ်မှတ်ထားပါတယ်။

---

````markdown
# 💻 Windows မှာ Kali Linux Install လုပ်နည်း (VirtualBox အသုံးပြုခြင်းဖြင့်)

> ဒီလမ်းညွှန်မှာတော့ Windows OS မှာ Kali Linux ကို Oracle VirtualBox အသုံးပြုပြီး Virtual Machine အနေနဲ့ Install လုပ်နည်းကို screenshot နှင့်အတူ ရှင်းလင်းပြထားပါတယ်။ Cybersecurity ကို စတင်လေ့လာမဲ့ Beginner များအတွက် ရည်ရွယ်ပါတယ်။

---

## 🛠️ လိုအပ်ချက်များ

| Tool | Description | Download Link |
|------|-------------|----------------|
| VirtualBox | VM Software | [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads) |
| Kali Linux ISO | Kali installer | [Download Kali ISO](https://www.kali.org/get-kali/#kali-platforms) |
| Windows PC | RAM 4GB+, Disk Space 20GB+ | - |

---

## 1️⃣ VirtualBox install လုပ်ခြင်း

1. [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads) မှာ windows အတွက် software ကို download ပြုလုပ်ပါ။
2. Installer ကို Run ပြီး Setup လုပ်ပါ။

<img src="images/1downloadvbox.png" alt="VirtualBox Download" width="600"/>

---

## 2️⃣ Kali Linux ISO ဖိုင် Download လုပ်ပါ

  - ဒီနေရာမှာ နည်းလမ်း ၂မျိုးရှိပါတယ်။ 
    1. ISO file ဖြင့် install လုပ်ခြင်း။
    2. OVA file ဖြင့် install လုပ်ခြင်း။

  <img src="images/2kalidownload.png" alt="Kali Linux ISO Download" width="600"/>


  ### ISO file ဖြင့် install လုပ်ခြင်း
  1. [Kali Linux Download Page](https://www.kali.org/get-kali/#kali-platforms) ကိုသွားပါ။
  2. Installer Images → 64-bit version ကို Download လုပ်ပါ။

  <img src="images/3kaliiso.png" alt="Kali Linux ISO Download" width="600"/>

---

## 3️⃣ Virtual Machine အသစ် Create လုပ်ပါ

1. VirtualBox ကိုဖွင့်ပြီး **New** ကိုနှိပ်ပါ။
2. Name: `Kali Linux`  
   Type: `Linux`  
   Version: `Debian (64-bit)`

<img src="images/step3_create_vm.png" alt="Create Kali VM" width="600"/>

---

## 4️⃣ RAM ထည့်ပါ

- အနည်းဆုံး: 2048 MB  
- အကြံပြု: 4096 MB

<img src="images/step4_set_ram.png" alt="Set RAM for VM" width="600"/>

---

## 5️⃣ Virtual Hard Disk ဖန်တီးပါ

- Create → VDI → Dynamically allocated → 80 GB+

<img src="images/step5_virtual_disk.png" alt="Create Virtual Disk" width="600"/>

---

## 6️⃣ Kali Linux ISO ဖိုင်ကို Attach လုပ်ပါ

1. Kali VM ကို ရွေးပြီး Settings → Storage ကို သွားပါ။
2. Empty CD icon ကိုရွေးပြီး ISO file ကို load လုပ်ပါ။

<img src="images/step6_attach_iso.png" alt="Attach Kali ISO" width="600"/>

---

## 7️⃣ VM ကို Start လုပ်ပါ

1. Start ကိုနှိပ်ပြီး VM boot တက်လာသည်ကိုစောင့်ပါ။
2. Menu ထဲက “Graphical Install” ကိုရွေးပါ။

<img src="images/step7_graphical_install.png" alt="Start Kali Graphical Install" width="600"/>

---

## 8️⃣ Kali Installation Setup

- Language, Location, Keyboard Layout တို့ကိုရွေးပါ။

<img src="images/step8_language.png" alt="Kali Language Selection" width="600"/>

- User, Hostname, Password ထည့်ပါ။

<img src="images/step8_user_config.png" alt="Kali User Setup" width="600"/>

---

## 9️⃣ Partitioning Disk

- Guided – Use Entire Disk → All files in one partition

<img src="images/step9_partition.png" alt="Partitioning Kali Disk" width="600"/>

---

## 🔁 Installation Process

- System Installing...
- GRUB bootloader ကို Yes ပြီး `/dev/sda` သို့ Install ပြုလုပ်ပါ။

<img src="images/step10_grub.png" alt="GRUB Bootloader Install" width="600"/>

---

## ✅ Finish Installation

- Installation ပြီးသွားပါက Reboot ဖြစ်ပြီး Kali ကို စတင်အသုံးပြုနိုင်ပါပြီ။

<img src="images/step11_finished.png" alt="Kali Installed Successfully" width="600"/>

---

  ### OVA file ဖြင့် install လုပ်ခြင်း
  1. [Kali Linux Download Page](https://www.kali.org/get-kali/#kali-platforms) ကိုသွားပါ။
  2. Virtual Machine → virtualbox → ကို Download လုပ်ပါ။
  3. VirtualBox ကိုဖွင့်ပါ။ File > Import Appliance > source > ova file ကိုရွေးပေးလိုက်ပါ။

  <img src="images/step11_finished.png" alt="Kali Installed Successfully" width="600"/>

---
## 🧠 အသုံးဝင်သော အကြံပြုချက်များ

- Kali Full Screen လုပ်ချင်လျှင်:  
  **Devices → Insert Guest Additions CD image**
- Drag and Drop / Clipboard Sharing → Enable from **Settings > General > Advanced**
- Kali Update Command:
  ```bash
  sudo apt update && sudo apt upgrade -y
````

---

## 📎 YouTube Video (Coming Soon)

📽️ [YouTube Video Link ထည့်မည်](#)

---

## 📚 ကိုးကား

* [Kali Linux Docs](https://www.kali.org/docs/)
* [VirtualBox Manual](https://www.virtualbox.org/manual/)

---

## 🙋 မေးမြန်းလိုတာများရှိပါက

* GitHub Issues မှာပြောနိုင်ပါတယ်။
* သို့မဟုတ် [PiiN Security](https://github.com/piin-security) ကိုလိုက်နာပါ။

```

---

### ✅ သတိထားရမည့်အချက်

- `images/` folder ထဲမှာ image files တွေကို သင့် GitHub Repo မှာတင်ဖို့လိုပါတယ်။
- အပေါ်မှာ link ထားတဲ့ image filenames တွေနဲ့ ကိုက်ညီအောင်ပေးရပါမယ်။
- မိမိရဲ့ screenshot များကို `.png` format နဲ့ images folder ထဲထည့်ပြီး တင်လို့ရပါတယ်။

---

**လိုအပ်ရင် ငါ zip format နဲ့ Markdown file + images folder ပေးလို့ရပါတယ်။ ပြောပေးပါ။**
```
