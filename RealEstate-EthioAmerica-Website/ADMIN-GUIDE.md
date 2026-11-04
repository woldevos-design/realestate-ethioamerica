# RealEstate EthioAmerica website: go-live and admin guide

This folder is the complete website. It has no monthly software cost: it runs on Netlify's free plan, and the admin panel (Decap CMS) is free and open source. You only pay for a domain name (about $15–20 a year).

**What's in the folder**

| Folder or file | What it is |
| --- | --- |
| `index.html` | The website (all pages) |
| `content/` | All the words, links and settings. The admin panel edits these files for you |
| `img/` | Photos and magazine pages. New uploads go to `img/uploads/` |
| `admin/` | The admin panel, at `yoursite.com/admin/` |
| `netlify.toml` | Hosting settings. Leave it as is |

---

## Part 1: Put the site live (one time, about 45 minutes)

You need: a free GitHub account, a free Netlify account, and later your domain.

1. **Create a GitHub repository.** Sign up at github.com, click **New repository**, name it `realestate-ethioamerica`, choose **Private**, and create it.
2. **Upload the files.** In the new repository click **uploading an existing file**, then drag in *everything inside* this folder (not the folder itself), including the `admin`, `content` and `img` folders. Click **Commit changes**.
3. **Connect Netlify.** Sign up at netlify.com with your GitHub account. Click **Add new site → Import an existing project → GitHub**, pick the repository, leave the build settings empty, and click **Deploy**. In about a minute you get a live address like `something.netlify.app`.
4. **Turn on the admin login.**
   - In Netlify open your site → **Project configuration → Identity** → **Enable Identity**.
   - Under **Registration**, choose **Invite only**.
   - Under **Services → Git Gateway**, click **Enable Git Gateway**.
   - Go to the **Identity** tab and click **Invite users**. Invite yourself and Binyam by email.
5. **Accept the invite.** Open the email, click the link, set a password. You land in the admin panel. From now on log in at `yoursite.com/admin/`.
6. **Connect your domain.** Buy the domain once you've settled the name (cover vs back cover). In Netlify go to **Domain management → Add a domain** and follow the steps. Netlify adds free HTTPS automatically.
7. **Turn on the forms.** In the admin panel open **Site settings**, tick **Turn on website forms**, untick **Show the preview banner**, and publish. Then in Netlify go to **Forms → Form notifications** and add an email notification so every inquiry lands in your inbox. Netlify's free plan has a monthly submission limit; check your plan in the Netlify dashboard.

> If the Identity option is not available on your account, the fallback is to log in with GitHub instead: in `admin/config.yml` change `name: git-gateway` to `name: github` and add a line `repo: YOUR-GITHUB-NAME/realestate-ethioamerica`. Each editor then needs a GitHub account with access to the repository.

---

## Part 2: Using the admin panel

Log in at `yoursite.com/admin/`. You'll see four sections on the left:

| Section | What you change there |
| --- | --- |
| **Advertisers** | Every developer, bank, attorney, architect, insurance agent and US agent: name, text, ad images, facts, areas, contact buttons, featured on home page, and the date their package ends |
| **News** | Stories for the News page, and the Coming Soon list |
| **Magazine issue** | The current issue's page images, table of contents, flipbook link and PDF, plus past issues |
| **Site settings** | Home page cover photo and headline (English and Amharic), disclaimers, contact channels, publishers, ad packages and prices |

**How saving works:** you edit, click **Save** (a draft), then open the **Workflow** tab and move the card to **Ready**, then **Publish**. The live site updates about a minute later. Nothing goes live by accident.

**Pictures:** click any image field, then **Upload**. Use JPGs under about 500 KB; magazine pages around 1000 pixels tall look sharp and load fast.

**An advertiser's package ended:** their profile hides itself automatically after the **Ad package ends on** date. To hide one early, untick **Show on website**.

---

## Part 3: Quarterly update checklist

Do this when each new issue comes out.

- [ ] **Magazine issue:** move the current issue into **Past issues** (title, cover, flipbook link, PDF).
- [ ] **Magazine issue:** set the new title (e.g. "Issue 02 · April 2027"), upload the new page images in order, update the table of contents, add the Flipsnack link and PDF.
- [ ] **Site settings → Home page cover:** new cover photo, issue label and headline, in English and Amharic.
- [ ] **Advertisers:** add new advertisers (only after they've given you every document on the Listing Standards list), update returning ones with their new ad image, and set each package's end date.
- [ ] **Advertisers:** tick **Featured** for the developers on this issue's Feature package (up to 4 show on the home page).
- [ ] **News:** add 2–3 new stories, mark any paid story as **Sponsored**, refresh the Coming Soon list.
- [ ] **Words check:** search every new text for verified, vetted, guaranteed, trusted, certified, approved, risk-free, safe investment, "we sell", "our listings". Replace them (see the table below).
- [ ] **Look at the live site on your phone** before you share the link.

**Words to avoid, and what to use instead**

| Avoid | Use instead |
| --- | --- |
| Verified, vetted, certified, approved | Selected, featured, advertiser-provided |
| Guaranteed, risk-free, safe investment | Advertised terms, according to the advertiser |
| Trusted, recommended, endorsed, best | Featured developer, selected advertiser |
| We sell, we broker, our listings, buy through us | Contact the advertiser directly |
| Commission, referral fee | Flat advertising fee |

---

## Before launch, still to do

- Attorney review of the disclaimers, Privacy Policy and Terms of Use (placeholders are on the Disclaimer page).
- Your translator reviews all Amharic text.
- Confirm each advertiser's phone, email and facts with them.
- Add your contact email, WhatsApp and Telegram channel links in **Site settings**.
- Ask Peg whether your KW name and license should appear anywhere.
