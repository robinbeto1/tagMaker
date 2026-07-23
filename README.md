# Associate Name Tag Maker

A free, self-contained web app for creating warehouse/fulfillment associate name tags with department training indicators.

## Features

- 🟢 **Green tags** for Seasonal / Temporary associates
- 🔵 **Blue tags** for Permanent associates
- Toggle trained departments (PICK, WS, PS, LA, SD, ARSAW, STOW, PACK, PP, PG, AFM, SINGLES, RECEIVE)
- Upload associate photo
- Live preview of badge
- Save multiple tags in one session
- **Bulk-generate badges from a CSV file** — one row per associate
- **Download all saved tags as a .docx Word file** — ready to print

## How to Use

### One at a time

1. Enter associate's **Last Name, First Name**
2. Enter their **Username / ID**
3. Select **Employment Type** (Seasonal or Permanent)
4. Optionally upload a **photo**
5. Click department buttons to mark **trained areas**
6. Click **＋ Save Tag** to queue the badge
7. Repeat for all associates
8. Click **⬇ Download Saved Tags (.docx)** to export a Word file

### In bulk, from a CSV

1. Click **⬇ Download Sample Template** to grab a starter CSV.
2. Fill in one row per associate using these columns (a header row is optional):

   | Column | Required | Notes |
   |---|---|---|
   | Name | Yes | `Last, First` |
   | Username | No | |
   | Manager | No | |
   | Type | No | `temp` or `perm` (defaults to temp) |
   | Days | Only for `perm` | e.g. `Mon,Tue,Wed,Thu,Fri` |
   | Departments | No | e.g. `PICK,WS,STOW` — unrecognized codes are ignored |

3. Click **⬆ Upload CSV & Generate Badges** and select the file — a badge is generated for every valid row and added to Saved Tags.
4. Photos aren't part of the CSV, so bulk-generated badges use the placeholder photo icon; download the .docx as usual once ready.

## Departments

| Dept | Dept | Dept |
|------|------|------|
| PICK | WS | PS |
| LA | SD | ARSAW |
| STOW | PACK | PP |
| PG | AFM | SINGLES |
| RECEIVE | | |

## Deployment

This is a single-file app — no build step, no server needed.

**GitHub Pages:** Upload `index.html` to a repo and enable Pages under Settings → Pages → Deploy from branch.

**Netlify Drop:** Drag `index.html` to [netlify.com/drop](https://app.netlify.com/drop).

## Tech

- Pure HTML / CSS / JavaScript — zero dependencies at runtime
- JSZip bundled inline for .docx ZIP generation
- Office Open XML generated natively in the browser
- No data ever leaves your browser
