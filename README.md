# WebRegScraper
A WebReg scraper that scrapes important information regarding **major/minor/honors** requirements not found in the SOC API or any other public-facing Rutgers API. This is a project built primarily for automatically creating core requirements for [**Scarlet Navigator**](https://scarletnav.io). However, there are other experimental WebReg data that can be scraped as well.

It scrapes Webreg information by logging into WebReg using a headless Chrome/Chromium browser via Pupeteer, compiling important data into a `json` file that is general and parsable by the **Scarlet Navigator** project.

# Getting Started
Make sure you have the following installed:

- [Node.js](https://nodejs.org/en/)
- [Puppeteer](https://pptr.dev/)
- [Git](https://git-scm.com/downloads)

Furthermore, you will **need to be** affiliated with Rutgers University in order to log into WebReg (e.g. student, facutly, staff). You may be prompt with a DuoPush notification on your phone to verify your identity. To get started, clone the repository and install the dependencies:

```bash
git clone git@github.com:openscarletorg/ScarletCourse.git
cd WebRegScraper
npm install
```

Then, you will need to modify the `.env` file to include your NetID and password.

```bash
NETID=YOUR_NETID
PASSWORD=YOUR_PASSWORD
```

# Running the Scraper
To run the scraper, simply run the following command:

```bash
node index.js --major
```

This will scrape the WebReg data for all majors and output the data into a `json` file. You can also run the scraper for minors and honors programs by using the `--minor` and `--honors` flags respectively.

