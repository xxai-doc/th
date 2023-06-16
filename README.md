<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

ส่วนหนึ่งของรหัสเว็บไซต์เป็นโอเพ่นซอร์ส ยินดีช่วยเพิ่มประสิทธิภาพการแปล

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
