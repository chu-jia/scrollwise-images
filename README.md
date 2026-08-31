# scrollwise-images

Public image hosting for the **ScrollWise** narrative arm (MobileCoach pilot).

Images are opened in the app via participant variables such as `$imageD2S1` (GitHub **raw** URLs + `show-web`). Inline chat teasers still use MobileCoach **Upload**; this repo stores **person-specific** chapter images.

## Repository layout

```text
scrollwise-images/
├── README.md
├── static_image/              # Shared / fallback images (optional)
└── participants/
    ├── test1/
    │   ├── d2s1.png
    │   ├── d2s2.png
    │   └── …
    ├── test2/
    │   └── d2s1.png
    │   └── …
    └── test3/
    │   └── d2s1.png
    │   └── …
    ├── …
```

### Naming


| Item               | Convention                                                           |
| ------------------ | -------------------------------------------------------------------- |
| Participant folder | Same as MobileCoach test name / ID (e.g. `chu`, `roy`) |
| Session files      | `d2s1.png` … `d2s5.png`, `d3s1.png` … `d4s5.png`                     |
| Format             | PNG or JPG, ideally **1024×1024**                                    |




## Direct links (use these in Participants)

**Do not** use the GitHub page URL (`…/blob/…`). Use **Raw** or jsDelivr.

### Raw (official)

```text
https://raw.githubusercontent.com/chu-jia/scrollwise-images/main/participants/<id>/d2s1.png
```

Example:

```text
https://raw.githubusercontent.com/chu-jia/scrollwise-images/main/participants/chy/d2s1.png
```



### jsDelivr (optional CDN)

```text
https://cdn.jsdelivr.net/gh/chu-jia/scrollwise-images@main/participants/<id>/d2s1.png
```



### Check before pasting into MobileCoach

1. Open the link in a new browser tab.
2. The page must show **only the image** (no GitHub UI).
3. Paste into Participants → `$imageD2S1` (or `$imageD2S2` …).



## How images are used in the study

1. Day 1: participant chooses preferences (`$protagonistName`, `$genrePref`, `$narrativeRole`, `$analogyDomain`).
2. Generate personalized chapter images (GPT Image) using those values.
3. Upload here under `participants/<id>/`.
4. Set the matching `$imageD…` variable in MobileCoach **Participants**.
5. In-app: after the story, **Open image** runs `show-web $imageD2S1 …`.



## Privacy

- Do **not** upload real photos of participants or identifiable personal data.  
- Use illustrated third-party protagonists (Sam / Lily) only.  
- Prefer non-identifying folder names if publishing beyond the pilot team.



## Maintainer

Chu Jia — UZH master’s thesis · ScrollWise narrative pilot
