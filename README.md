# fiverr-alarm-ping

GitHub Actions দিয়ে Render সার্ভার প্রতি ৫ মিনিটে ping করে জাগিয়ে রাখে।

## কীভাবে কাজ করে

`.github/workflows/ping.yml` — প্রতি ৫ মিনিটে `/health` endpoint-এ GET request পাঠায়।

## Setup

Repository Settings → Secrets and variables → Actions → New repository secret:
- `HEALTH_URL` = `https://তোমার-অ্যাপ.onrender.com/health`

## সতর্কতা

GitHub Actions schedule ৬০ দিন কোনো commit না থাকলে বন্ধ হয়ে যায়।
প্রতি ২ মাসে একবার এই ফাইলে যেকোনো ছোট পরিবর্তন করে commit দাও।
