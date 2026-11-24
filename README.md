# BazarDor daily TCB prices

বাজারদর অ্যাপের জন্য টিসিবির দৈনিক খুচরা বাজার দর, প্রতিদিন হালনাগাদ হয়।
The daily retail price ranges from TCB that the BazarDor app uses, updated every day.

**File:** [`official-prices.json`](official-prices.json)
**Address the app downloads:** https://abedinm.github.io/bazardor-prices/official-prices.json

## বাংলা

- দামগুলো **ট্রেডিং কর্পোরেশন অব বাংলাদেশ (টিসিবি)**-এর, [tcb.gov.bd](https://tcb.gov.bd/pages/daily-rmps) থেকে নেওয়া।
  প্রতিটি দামের সাথে টিসিবির মূল ফাইলের লিংক আছে।
- এখানে বাজারদর অ্যাপের আটটি পণ্যের গত ৯০ দিনের সর্বনিম্ন ও সর্বোচ্চ দাম আছে।
  ডিমের দাম হালি থেকে ডজনে রূপান্তর করা, আর কিছু বদলানো হয়নি।
- একটি স্বয়ংক্রিয় কাজ প্রতিদিন সন্ধ্যা সাড়ে ৫টায় (ঢাকা) নতুন তালিকা যোগ করে।
  এতে টিসিবির ওয়েবসাইটে দিনে সাধারণত দুটি অনুরোধ যায়।
- **এটি সরকারি তথ্যসূত্র নয়।** বাজারদর একটি বেসরকারি অ্যাপ, বাংলাদেশ সরকার বা টিসিবির সাথে যুক্ত নয়।
  সরকারি দামের জন্য সবসময় tcb.gov.bd দেখুন।
- এখানে কারও ব্যক্তিগত তথ্য নেই।

## English

- The prices are published by the **Trading Corporation of Bangladesh (TCB)** at
  [tcb.gov.bd](https://tcb.gov.bd/pages/daily-rmps). Every range links to the TCB file it came from.
- The file holds the lowest and highest Dhaka retail price of BazarDor's eight items for the last
  90 days. Egg prices are converted from per hali (4 eggs) to per dozen; nothing else is changed.
- An automated job adds TCB's new list every day at 17:30 Dhaka time. It normally makes two
  requests a day to tcb.gov.bd: the listing page and the new file.
- **This is not an official source.** BazarDor is an unofficial app, not made by or connected with
  the Government of Bangladesh or TCB. For official prices, always check tcb.gov.bd.
- TCB's site states no terms for reusing these figures. If TCB asks for any change, or for the
  data to be removed, it will be done promptly.
- The file contains no personal information about anyone.

## Format

JSON, one price range per line so the daily change is easy to read in the history:

```json
{"version":1,"source":"tcb","attribution":"...","generated_at":"2026-11-24T17:30:00+06:00","newest_date":"2026-11-24","ranges":[
{"item":"Onion (Local)","date":"2026-11-24","min":45.0,"max":55.0,"source_url":"https://..."},
...
]}
```

| Field | Meaning |
|---|---|
| `item` | BazarDor's item name |
| `date` | The day of TCB's list (YYYY-MM-DD) |
| `min`, `max` | Lowest and highest price in taka, per kg, litre or dozen |
| `source_url` | The TCB file the range came from |
