# Fake Profile Detection using ANN

This project aims to detect fake profiles on social media or online platforms using an **Artificial Neural Network (ANN)** model. It helps in identifying patterns and anomalies in user behavior, profile details, and activity history to classify profiles as fake or genuine.

---









test.js
const { Builder, By, Key } = require('selenium-webdriver');

async function testExample() {
    // 1. Launch Chrome Browser
    let driver = await new Builder().forBrowser('chrome').build();

    try {
        // 2. Open a webpage
        await driver.get('https://www.google.com');

        // 3. Find an element (search box)
        let searchBox = await driver.findElement(By.name('q'));

        // 4. Type text into the element
        await searchBox.sendKeys('Selenium WebDriver Testing', Key.RETURN);

        // 5. Get the title of the page
        const title = await driver.getTitle();
        console.log("Page Title:", title);

        // 6. Wait for results
        await driver.sleep(3000);

        console.log("Test Completed Successfully");

    } catch (error) {
        console.log("Error occurred:", error);
    } finally {
        // 7. Close the browser
        await driver.quit();
    }
}

testExample();








dockerfile
FROM node:18-alpine

# set working directory inside the image
WORKDIR /app

# copy package files & source into the image
COPY . .

# install production dependencies (yarn is available via corepack in Node 18)
RUN yarn install --production

# expose port (documentation only — container still needs run -p to bind host port)
EXPOSE 3000

# command to start the app
CMD ["node", "src/index.js"]







git clone https://github.com/docker/getting-started-app.git 
