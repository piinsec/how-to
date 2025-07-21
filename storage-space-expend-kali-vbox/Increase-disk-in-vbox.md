# VirtualBox မှာ Kali ရဲ့ storage space ကို ဘယ်လိုချဲ့မလဲ?
> Kali linux ကို Virtual box မှာသုံးနေရင်းနဲ့ storage မလောက်တဲ့ ပြဿနာကို ကြုံတွေ့နေတယ်ဆိုရင် ဒီနည်းလမ်းနဲ့ ဖြေရှင်းလို့ရပါတယ်။

## Step 1

- VirtualBox ရဲ့ File menu ထဲက Tools ကို ထဲက Virtual Media Manager ကိုရွေးလိုက်ပါ။

  <img src="images/kali1.png" alt="VirtualBox Download" width="600"/>

- Hard disks tab အောက်ထဲ က ကိုယ် storage တိုးမဲ့ virtual disk ကို Double click နှိပ်လိုက်ပါ။ (eg: kali.vdi)
- အောက်က Attributes tab ထဲက size မှာ ကိုယ်လိုချင်သလောက်တိုးလို့ရပါပီ။

  <img src="images/kali2.png" alt="VirtualBox Download" width="600"/>

## Step 2

- VirtualBox က Kali machine ကို start လုပ်လိုက်ပါ။
- Terminal က နေ “gparted” ကို ရိုက်လိုက်ပါ။
- ခုနက တိုးထားတဲ့ disk space က unallocated space ဖြစ်နေပါလိမ့်မယ်။

  <img src="images/kali3.png" alt="VirtualBox Download" width="600"/>

- အဲ့ဒါကို new partition (သို့) ရှိပြီးသား partition ကို extend လုပ်လို့ရပါတယ်။
- ရှိပြီးသား /dev/sda1 ကို extend လုပ်ချင်တယ်ဆိုရင်တော့ /dev/sda2 အောက်မှာရှိတဲ့ linux-swap ကို အရင်ဖျက်ပြီး /dev/sda2 ကိုလည်းဖျက်ပစ်ဖို့လိုပါတယ်။
- linux-swap ကိုဖျက်ဖို့ right click နှိပ်ပြီး swapoff အရင်လုပ်ရပါတယ်။ပြီးမှ Delete လုပ်လိုက်ပါ။
- /dev/sda1 ကို resize လုပ်ပါ။ swap အတွက် 2GB လောက်ချန်ထားပါ။
- ကျန်တဲ့ 2GB ကို right click နှိပ် new ဆိုပြီး file system မှာ linux-swap ဆိုပြီးရွေးပေးလိုက်ပါ။
- အားလုံးပြီးသွားတဲ့အခါ tool bar က အမှန်ခြစ်လေးကိုနှိပ်ပေးလိုက်ပါ။
- အပေါ်က လုပ်ခဲ့တဲ့ အဆင့် တွေအားလုံး ကို ပေါင်းလုပ်သွားမှာဖြစ်ပါတယ်။
- Linux-swap ကို right click နှိပ်ပြီး swapon ပြန်လုပ်ပေးလိုက်ပါ။

  <img src="images/kali4.png" alt="VirtualBox Download" width="600"/>

VirtualBox မှာ Kali linux ရဲ့ storage တိုးတဲ့ လုပ်ငန်းစဉ်ပြီးသွားပါပီ။
