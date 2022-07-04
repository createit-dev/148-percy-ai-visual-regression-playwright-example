# Percy AI visual regressions - playwright example
### Example of e2e test in Playwright that will generate percy.io snapshot

Percy provides way to compare screenshots against the baseline. Screenshots are tested in the cloud using 4 most popular browsers: Chrome, Firefox, Edge and Safari. 

We can also define width breakpoints to test smaller resolutions. Under the hood - Google Kubernetes in Google Cloud Platform are used for visual comparison. New screens are compared to previously approved “Baseline screens”.

NPM package @percy/cli is used to create snapshots of website. Already generated DOM html code and assets are send to percy API and site is recreated in the cloud container and render again in most popular browsers. Advantage of this solution is that: website don't need to be publicly available! You can easily – just point to your localhost url and screenshot will be generated successfully!

## Getting started
1. Install dependencies:

`npm install`

`npx playwright install`

2. Configure percy

`export PERCY_TOKEN=abcd1234`

### Configuration
Setup breakpoints and custom CSS in percy.yml file

### Commands
Run standard playwright tests:
`npx playwright test test1`

Run percy snapshots:
`npm run runpercy_test1`
<br/>
(results will be visible in Percy.io dashboard within minutes)

### Dependencies
Node: v16.15.1 or earlier

![](https://github.com/createit-dev/148-percy-ai-visual-regression-playwright-example/blob/main/images/percy_io_playwright_example.gif)
