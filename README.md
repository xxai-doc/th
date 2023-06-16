<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

ขอแนะนำให้ติดตั้ง nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) ก่อน จากนั้นจึง `direnv allow` หลังจากเข้าสู่ไดเร็กทอรี ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) จะถูกดำเนินการโดยอัตโนมัติหลังจากเข้าสู่ไดเร็กทอรี)

ความหมายคือ: การแปลภาษาจีนเป็นภาษาญี่ปุ่น ภาษาเกาหลี ภาษาอังกฤษ การแปลภาษาอังกฤษเป็นภาษาอื่นๆ ทั้งหมด หากคุณต้องการรองรับเฉพาะภาษาจีนและอังกฤษ คุณก็เขียน `zh: en` ได้เลย

## รหัสส่วนหน้า

* [รหัสส่วนหน้า](https://github.com/xxai-art/web)
* [ชุดภาษาสำหรับไซต์โดยรวม](https://github.com/xxai-art/web/tree/main/i18n)
* [ชุดภาษาสำหรับโมดูลการเข้าสู่ระบบ](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [เอกสารหลายภาษาของเว็บไซต์](https://github.com/xxai-doc)

ภาษาการเขียนโปรแกรมส่วนหน้าคือ [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) ซึ่งเพิ่มคุณลักษณะบางอย่างตามไวยากรณ์ของสคริปต์กาแฟ โปรดดูที่ . [/coffee_plus.md](./coffee_plus.md)

## การทำเว็บไซต์และเอกสารให้เป็นสากล

สร้างจาก 3 โครงการต่อไปนี้

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  คำต่อท้ายคือ `.mdt` คุณสามารถใช้ไวยากรณ์ที่คล้ายกับ `<+ ./coffee_plus/import.js>` เพื่ออ้างถึงไฟล์ภายนอก และสร้างมาร์กดาวน์ด้วยคำต่อท้าย `.md`

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  การแปลแบบ Markdown จะไม่แปลรหัสและลิงก์ และจะแคชประโยคที่แปล หากมีการแก้ไขคำแปลแต่ข้อความต้นฉบับไม่ได้แก้ไข การดำเนินการอีกครั้งจะไม่เขียนทับการแก้ไขการแปล

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  ไฟล์ภาษาสำหรับแปลเว็บไซต์ที่สร้างโดย `yaml`

### คำแนะนำการแปลเอกสารอัตโนมัติ

ดูที่เก็บโค้ด [xxai-art/doc](https://github.com/xxai-art/doc)

ขอแนะนำให้ติดตั้ง nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) ก่อน จากนั้นจึง `direnv allow` หลังจากเข้าสู่ไดเร็กทอรี ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) จะถูกดำเนินการโดยอัตโนมัติหลังจากเข้าสู่ไดเร็กทอรี)

เพื่อหลีกเลี่ยงโค้ดเบสขนาดใหญ่ที่แปลเป็นภาษาต่างๆ หลายร้อยภาษา ฉันจึงสร้างโค้ดเบสแยกต่างหากสำหรับแต่ละภาษาและสร้างองค์กรเพื่อจัดเก็บโค้ดเบส

การตั้งค่าตัวแปรสภาพแวดล้อม `GITHUB_ACCESS_TOKEN` จากนั้นเรียกใช้ [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) จะสร้างที่เก็บรหัสโดยอัตโนมัติ

แน่นอน คุณยังสามารถใส่ไว้ในรหัสฐาน

การอ้างอิงสคริปต์การแปล [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

รหัสสคริปต์ถูกตีความดังนี้:

[bunx](https://bun.sh/docs/cli/bunx) มาแทน npx ซึ่งเร็วกว่า แน่นอน หากคุณไม่ได้ติดตั้ง bun ไว้ คุณสามารถใช้ `npx` แทนได้

`bunx mdt zh` แสดงผล `.mdt` ในไดเร็กทอรี zh เป็น `.md` ดูไฟล์ที่เชื่อมโยง 2 ไฟล์ด้านล่าง

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` เป็นโค้ดหลักสำหรับการแปล (หากคุณติดตั้งเฉพาะ `nodejs` แต่ไม่ได้ติดตั้ง `bun` และ `direnv` คุณสามารถเรียกใช้ `npx i18n` เพื่อแปลได้)

มันจะแยกวิเคราะห์ [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) การกำหนดค่าของ `i18n.yml` ในเอกสารนี้เป็นดังนี้:

```
en:
zh: ja ko en
```

ความหมายคือ: การแปลภาษาจีนเป็นภาษาญี่ปุ่น ภาษาเกาหลี ภาษาอังกฤษ การแปลภาษาอังกฤษเป็นภาษาอื่นๆ ทั้งหมด หากคุณต้องการรองรับเฉพาะภาษาจีนและอังกฤษ คุณก็เขียน `zh: en` ได้เลย

สุดท้ายคือ [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) ซึ่งแยกเนื้อหาระหว่างชื่อหลักและคำบรรยายแรกของแต่ละภาษา `README.md` เพื่อสร้างรายการ `README.md` รหัสนั้นง่ายมากคุณสามารถดูได้ด้วยตัวคุณเอง

Google API ใช้สำหรับการแปลฟรี หากคุณไม่สามารถเข้าถึง Google ได้ โปรดกำหนดค่าและตั้งค่าพร็อกซี เช่น:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

สคริปต์การแปลจะสร้างแคชที่แปลแล้วในไดเร็กทอรี `.i18n` โปรดตรวจสอบ `git status` และเพิ่มลงในที่เก็บโค้ดเพื่อหลีกเลี่ยงการแปลซ้ำ

โปรดเรียกใช้ `bunx i18n` ทุกครั้งที่คุณแก้ไขการแปลเพื่ออัปเดตแคช

หากข้อความต้นฉบับและการแปลถูกแก้ไขพร้อมกัน แคชจะสับสน ดังนั้นหากคุณต้องการแก้ไข คุณสามารถแก้ไขได้เพียงรายการเดียว จากนั้นเรียกใช้ `bunx i18n` เพื่ออัปเดตแคช
