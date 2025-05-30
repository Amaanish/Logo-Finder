# Website Logo Extractor

This Python script is designed to fetch the logo image URL from a given website. It uses the `requests` library to download the webpage and `BeautifulSoup` to parse the HTML.

##  How It Works

The `get_logo_url` function scans all `<img>` tags and checks whether the `alt` attribute or the class name contains the word **"logo"**. If found, it returns the absolute URL of the image using `urljoin` to combine the base website URL and the image's `src`. If no such image is found or an error occurs, it returns a relevant message.

The `urlin` function prompts the user to input a website URL, which is then passed to `get_logo_url`.


However, this script does not work for some websites due to several technical reasons:

1. JavaScript Rendering: It can’t detect logos loaded dynamically via JavaScript since it only fetches static HTML.

2. Non-descriptive Tags: If the image doesn’t have “logo” in its alt or class, it won’t be detected.

3. CSS Background Logos: Logos set as background images in CSS won’t appear in HTML <img> tags.

4. Bot Protection: Some sites block or alter responses to automated requests.

5. Lazy Loading or Malformed URLs: Logos using data-src or unusual paths may be missed.

These are the technical limitations of the script in real-world applications. To improve it, one might need to incorporate a headless browser (like Selenium or Playwright), analyze CSS for background images, or improve image heuristics with machine learning.

## How to run the program:

``` bash
git clone https://github.com/Amaanish/Logo-Finder.git
```
Import the .ipynb file into Google Collab or Jupyter

Run the program and copy and paste the link to find the logo images.

