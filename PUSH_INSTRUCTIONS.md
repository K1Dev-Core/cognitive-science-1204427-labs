# วิธีอัปขึ้น GitHub (public) — เหลือกดแค่ไม่กี่คำสั่ง

> ผมเตรียมไฟล์ทั้งหมด + README + .gitignore ไว้ในโฟลเดอร์นี้ให้แล้ว
> แต่สร้าง repo บน GitHub แทนไม่ได้ (ต้องใช้บัญชีของคุณ) เลยขอให้รันคำสั่งด้านล่างเองครับ

เปิด Terminal แล้ว:

```bash
cd ~/Downloads/cognitive-science-1204427-labs
git init
git add -A
git commit -m "Cognitive Science (1204 427) labs 01-20 + mini-project"
```

## ทางเลือก A — มี GitHub CLI (`gh`) แล้ว (ง่ายสุด)
```bash
gh repo create cognitive-science-1204427-labs --public --source=. --remote=origin --push
```
เสร็จ! repo จะเป็น public ทันที

## ทางเลือก B — ใช้ git ธรรมดา
1. ไปสร้าง repo เปล่า (public) ที่ https://github.com/new ชื่อ `cognitive-science-1204427-labs` (อย่าติ๊ก add README)
2. แล้วรัน (แทน `<user>` ด้วยชื่อบัญชีคุณ เช่น K1Dev-Core):
```bash
git branch -M main
git remote add origin https://github.com/<user>/cognitive-science-1204427-labs.git
git push -u origin main
```

เท่านี้ก็ขึ้น GitHub แบบ public ครบทุกงานครับ
