# Real World Testing with Cypress Blog

A Next.js Blog for the Real World Testing with Cypress Curriculum.

## Key Takeaways

- Wrap returned values from requests to be able to work with them directly
- Can `invoke` methods such as `slice` by name and with arguments in a different form than usual
  ```js
  cy.wrap(res.body).invoke('slice', 0, 1)
  ```
- Use `.its(number)` to get the value of an array at index 'number'
- and `.its('attr')` to get the attribute of that element

## Other Notes

Added jsconfig.json with options
```json
{
  "compilerOptions": {
    "types": ["cypress"]
  }
}
```
to stop the auto-import of the wrong package every time `cy.` was typed

The network request specs do not work because the page '/network' does not exist

## Installation

```bash
yarn install
```

Start the local dev server.

```bash
yarn dev
```

While the dev server is running, in a separate terminal window, run the following command to launch Cypress.

```bash
yarn cypress:open
```

## Pratice Tests & Answers

The practice tests are located in `cypress/integration/Practice`

The answers are located in `cypress/integration/Answers`

---

This repo is a fork of the [Next.js Learn Starter](https://github.com/vercel/next-learn-starter/)
