# Renew

Renew is an Android app. You type the recurring payments you want to remember. The home screen shows what they cost this month and this year, and the app reminds you before the next charge.

The list stays on the phone. Renew does not connect to a bank. Five payments are free. Unlimited is a single Google Play purchase. Google shows the price with VAT included.

This document is the plan. The repository front page is [README.md](README.md). Released changes go in [CHANGELOG.md](CHANGELOG.md).

## People

Alex pays for Spotify, a gym, a phone contract, Netflix, iCloud, and a news site. The phone's own subscription screen shows only the ones bought from Google. Alex will not give a banking password to another app.

Renew is for that person. They keep it if adding those six takes about two minutes, the first screen states a clear monthly total, and a reminder arrives before the gym renews.

Free iPhone trackers already exist. Renew is the Android app for people who also want a single purchase, a list that includes the gym and the phone contract, and no bank login.

## Application id

The application id is `pro.ixrqq.renew`.

A Play application id is the domain you control, reversed, then the app name. Netflix owns `netflix.com`, so the Android TV app is `com.netflix.ninja`: `com.netflix` from the domain, `ninja` as that app's name. Renew uses the same rule. The domain is [ixrqq.pro](https://www.ixrqq.pro/), so the id is `pro.ixrqq` plus `renew`.

`ie.qqrxi.renew` does not follow that rule. `qqrxi` is the Play account name, and `qqrxi.ie` is not a domain we control. The country where the app is sold does not go in the id. Ireland is covered by the legal section below, not by an `ie.` prefix.

`pro.ixrqq.renew` is also the Kotlin package. If an iOS build ever exists, the bundle id is the same string. After the first upload to Play, the id cannot change. A later company can receive the listing by a Play transfer. The id stays `pro.ixrqq.renew`.

The public store title is **Renew: Payment Reminders**, so a taken short name does not block the listing.

## What the first version does

Home shows three things: this month's total, this year's total, and the payments due in the next 7 days.

Adding a payment asks for the name, the amount, how often it repeats (week, month, or year), and the next charge date. A short list of common names fills the icon and a usual price, which the person can change. Netflix, Spotify, iCloud, gym, and phone are in that list. Category and colour are optional.

Each payment can be edited, paused, or marked cancelled. Cancelled payments leave the total. When a date passes, Renew asks "Did this renew?" and moves the date forward on yes.

The reminder is on the morning of the day, 3 days before the charge. Settings can change that to 1 day or 7 days. The app explains the reminder, then Android shows its notification permission dialog. Renew does not use the exact-alarm permission. Play allows that permission for alarm and calendar apps, and a morning reminder is the right behaviour here.

There is no account. An export file is the backup, and the same file can be imported onto a new phone. Android's own cloud backup is turned off for the payment database, so the list is not copied to Drive.

Light and dark mode are both in the first version. The currency follows the phone and can be changed in settings. Amounts the person typed are shown as they typed them.

Five payments are free. The Play purchase removes the limit and stays bought. The button says what the purchase unlocks. The Play sheet shows the price.

## Layout

Phone first. One column, a large total, and a bottom bar with Home, Upcoming, and Settings. The add button stays in thumb reach.

On a tablet or a wide window the total and the next 7 days stay on the left, and the full list sits on the right. The layout uses the width. It is not a stretched phone screen, and it does not hide the total.

Type is large. Space is generous. There is one accent colour. Common services get a simple icon. An empty home screen shows a sample total and one action, "Add your first payment".

The app opens from the database on the phone. The first screen does not wait on a network.

Text follows the phone's font size. Controls meet a normal touch size. Icons have labels for TalkBack. Contrast holds in light and dark.

## What stays out

These are product decisions. They are also what keeps the first version inside EU and Irish rules.

- No bank connection, no reading of texts, and no reading of email. People type each payment.
- No card number, IBAN, or password field.
- No account, no analytics, and no crash reporter. Adding any of those waits for a privacy review and a changelog note.
- No second checkout on the website. Play is the only place to pay, so Google handles the consumer VAT on the purchase.
- No claim that Renew finds forgotten charges, cancels a payment, or stops a company from billing.
- No financial advice. The person cancels with the company that charges them. A notification can fail to appear.
- No Irish-language interface in the first version. A private app has no duty to ship one.
- The app is not made for children. The Play listing says it is not designed for children.

## EU and Ireland

Sold from Ireland, on the Play account `qqrxi`, to people in the EU.

Renew stores names, amounts, and dates on the device. That information can describe someone's spending, so the privacy page explains it even though the developer does not receive a copy. Uninstalling the app, or deleting a payment, removes it. There is no server copy to erase.

A privacy page and a short terms page are linked from Play and from Settings. Both live on ixrqq.pro before anyone is charged. The pages carry no analytics, so they do not need a cookie banner. The privacy page names the developer, says the list stays on the phone, says Google handles the purchase, says how deletion works, and gives a contact email. Settings shows the developer name, Ireland, and that email.

The terms say what Renew does, that cancellation happens with the charging company, and that Irish law governs the contract. Consumers in other EU countries keep the mandatory rights of their home country.

Play's purchase flow supplies the digital unlock immediately. Play's terms record that the buyer agrees to that and gives up the automatic 14-day withdrawal for that digital content. Refunds follow Google Play's flow.

Charging for the unlock means the Play account is a trader. Declare trader status in Play Console before release. A personal account shows the address and phone number on the public listing. Every active Play account must make this declaration by 1 February 2027. Declaring non-trader while charging is unlawful and can remove the app.

The Data safety form matches the app: the list stays on the device, the developer does not collect it, and the developer does not share it. Purchases are Google's.

The app targets Android 16, API level 36. Play has required that for new apps since 31 August 2026.

Payout reports from Google are kept and declared to Revenue. This plan is not tax advice.

A solicitor reads the privacy page and the terms before the app goes on sale.

## Six weeks

About 10 hours a week. The agent writes the screens. A real phone and a wide window get checked by hand.

**Week 1. A screen people can react to.** Home, add, and list, with sample payments. Phone width and tablet width. Light and dark. Show it to 8 people who have subscriptions. Continue if 5 of them add their real ones and can say the monthly total.

**Week 2. The list becomes real.** Save on the device. Edit, pause, cancel, and "Did this renew?". Categories, search, and Upcoming.

**Week 3. Reminders and the purchase.** The explanation before the notification permission, the 1 / 3 / 7 day choice, the free limit of 5, the Play unlock, and backup turned off for the database. Export and import.

**Week 4. Finish the first version.** Icons for common services, empty states, a pass on a small phone and a tablet, and the Ireland check: locale, euro, large font. Privacy page, terms, and the Settings links. Five people use it for a week. Fix whatever made them stop opening it.

**Week 5. Play.** Listing on account `qqrxi`, application id `pro.ixrqq.renew`, title "Renew: Payment Reminders". Trader details, Data safety, content rating, API 36, and screenshots of the monthly total and the reminder. Internal testing, then production. The privacy and terms URLs are live first.

**Week 6. The first 20 people.** Friends, then a few posts where people talk about forgotten renewals. Goal: 20 phones with a real list, and 5 purchases. Their complaints decide the next version.

## After the first 20

Only if those people are still opening Renew at the end of week 6:

- A home-screen widget with the monthly total and the next charge.
- A second currency on the same list.
- One purchase covering a household, with a separate list on each phone.

A bank connection is a different product and is not on this list.

## Money

A finished utility can sell a few copies a week once the listing and the screenshots are clear. A similar pay-once tracker made about $1,000 from roughly 40 buyers in its first public month. Renew can land in that range, or below it, because free trackers already exist. The reasons to install this one are Android, the gym and the phone contract on the same list, the single Play purchase, and a home screen that states the monthly total.

## Versioning

Semantic versions, git tags, and `CHANGELOG.md` are defined in [README.md](README.md). The plan itself is version 0.1.0. The first installable build gets the next version, and its notes move out of `[Unreleased]` when that build is tagged.

## Repository

GitHub: https://github.com/robertf670/renew

Local project: `Documents/projects/renew`.
