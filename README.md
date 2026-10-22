# FMCreators Marketplace (FMC)

**Live site: [fmc.xsrazy.web.id](https://fmc.xsrazy.web.id)**

FMCreators Marketplace is the public catalog website of FM Creators, a Roblox clothing community. It presents a curated collection of Roblox clothing items ("Marketplace picks") in one clean, browsable place, with item images shown directly from their original source. Behind the public catalog sits a private admin dashboard used to manage the collection.

> **Note:** This repository is documentation only. It describes the website in detail; the source code is private and is not published here.

## Why This Exists

FM Creators designs and curates Roblox clothing, but Roblox's own catalog is enormous and noisy: finding good items means wading through endless search results, copies, and unrelated uploads. Members of the community kept asking for a simpler way to browse the pieces the community actually recommends.

FMC was built to answer that: a single curated storefront where every item in the list is there because it was picked for the catalog, not because an algorithm surfaced it. The catalog grew item by item into a collection of more than 1,700 Roblox clothing items (as of October 2026), all maintained in one database and presented through one fast website.

## Purpose

- Give the FM Creators community one trusted place to discover curated Roblox clothing items.
- Make browsing effortless: item names, types, and prices are stored in a structured catalog, so the collection can be searched, sorted, and filtered instead of scrolled blindly.
- Show every item exactly as it looks on Roblox, with thumbnails delivered straight from the original source.
- Keep catalog management practical for a one-person team, with bulk importing and automated checks doing the repetitive work.

## Features

**Public catalog**

- A curated storefront ("Marketplace picks") listing the full FM Creators selection of Roblox clothing items.
- Item names, types, and prices fetched and kept in a structured database, so the catalog stays consistent and searchable.
- Item images displayed directly from their original source (Roblox's own image delivery), so what you see is the real item artwork.
- A themed interface that matches the FM Creators brand identity, with full SEO and social-sharing metadata so catalog pages present properly when shared.

**Catalog management (private)**

- A private admin dashboard for managing the catalog: adding and editing items, and keeping the collection tidy.
- Fast bulk import of items from plain text lists, so hundreds of items can be added in one session instead of one by one.
- Automatic broken-thumbnail detection, which scans the catalog and flags items whose images no longer load.
- Assisted renaming on import: item names can be normalized into clean, keyword-style English names automatically during the import process, keeping the public catalog readable and consistent.

## Frontend

The public frontend is a fast, single-purpose catalog site: a branded header, the curated item grid, and straightforward browsing of the collection. Item artwork is served from the original source rather than copied locally, which keeps pages light and the images always current.

Alongside the public pages, the same application hosts the private management interface used by the site owner. It is not linked from the public catalog and is only for maintaining the data behind the scenes.

## Backend / How It Works

The backend is a set of API routes backed by a hosted Postgres database (Supabase):

- The catalog lives in a database table of items (name, type, price, thumbnail, and housekeeping fields). The public API serves the catalog from this table, so the website always reflects the current collection.
- A health endpoint reports the state of the catalog, including the total item count.
- Management actions run through protected API routes that are only available to the signed-in site owner. Public visitors only ever receive the published catalog data; internal housekeeping fields are never exposed through the public API.
- Bulk imports write items into the database in batches and run image checks against the original sources, so broken thumbnails are caught early instead of being discovered by visitors.

## Summary

FMCreators Marketplace is the curated front window of the FM Creators Roblox clothing community: a hand-picked, database-driven catalog of 1,700+ items with artwork straight from the source, maintained through a private dashboard built for bulk work.

## 🌐 Socials
[![Behance](https://img.shields.io/badge/Behance-1769ff?logo=behance&logoColor=white)](https://behance.net/xsrazy) [![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/xsrazy) [![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://facebook.com/xsrazy) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/xsrazy) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/xsrazy) [![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://medium.com/@xsrazy) [![Pinterest](https://img.shields.io/badge/Pinterest-%23E60023.svg?logo=Pinterest&logoColor=white)](https://pinterest.com/xsrazy) [![Quora](https://img.shields.io/badge/Quora-%23B92B27.svg?logo=Quora&logoColor=white)](https://quora.com/profile/xsrazy) [![Reddit](https://img.shields.io/badge/Reddit-%23FF4500.svg?logo=Reddit&logoColor=white)](https://reddit.com/user/xsrazy) [![Stack Overflow](https://img.shields.io/badge/-Stackoverflow-FE7A16?logo=stack-overflow&logoColor=white)](https://stackoverflow.com/users/31065073) [![Twitch](https://img.shields.io/badge/Twitch-%239146FF.svg?logo=Twitch&logoColor=white)](https://twitch.tv/xsrazy) [![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/xsrazy) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/c/xsrazy)

## 💰 You can help me by Donating
[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=plastic&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/xsrazy) [![PayPal](https://img.shields.io/badge/PayPal-00457C?style=plastic&logo=paypal&logoColor=white)](https://paypal.me/xsrazy) [![Patreon](https://img.shields.io/badge/Patreon-F96854?style=plastic&logo=patreon&logoColor=white)](https://patreon.com/Xsrazy) [![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=plastic&logo=ko-fi&logoColor=white)](https://ko-fi.com/xsrazy)
