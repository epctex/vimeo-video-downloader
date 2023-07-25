[https://apify.com/epctex/vimeo-video-downloader](https://apify.com/epctex/vimeo-video-downloader?fpr=yhdrb)

# Actor - Vimeo Video Downloader

## Vimeo Video Downloader

Since Vimeo doesn't provide a good and free API, this actor should help you to download videos from Vimeo.com

The Vimeo Video Downloader supports the following features:

-   Download Video - If you want to get videos on a certain URL, just type the URL.

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/vimeo-video-downloader/issues).


## Input Parameters

The input of this scraper should be JSON containing the list of pages on Vimeo.com that should be visited. Required fields are:

- `startUrls`: (Optional) (Array) List of Vimeo URLs. You should only provide post URLs.

- `quality`: (Optional) (String) Select the video quality. You can use `highest`, `medium`, and `lowest`.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

- `extendOutputFunction`: (Optional) (String) Function that takes a JQuery handle ($) as an argument and returns an object with data.

- `customMapFunction`: (Optional) (String) Function that takes each object's handle as an argument and returns the object with executing the function.

This solution requires using **Residential Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Tips

- You must use a residential proxy to fetch videos. 

- When you want to scrape over a specific list URL, just copy and paste the link as one of the **startUrl**.

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape as many items as possible. Therefore, it forefronts all the detailed requests. If the actor doesn't block very often it'll scrape 1 video under 45 seconds with ~0.01-0.02 compute units.

### Vimeo Video Downloader Input example

```json
{
  "startUrls": [
    "https://vimeo.com/731185961"
  ],
  "quality": "medium",
  "proxy": {
    "useApifyProxy": true
  }
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## Vimeo Video Downloader Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from Vimeo Video Downloader.

The structure of each item in Vimeo looks like this:

### Item Detail

```json
{
	"sourceUrl": "https://player.vimeo.com/video/731185961",
	"downloadUrl": "https://api.apify.com/v2/key-value-stores/d6179b2c-fd6d-4be0-8fa8-3b421044f2af/records/bac2c55506fe79014c959f0ba41d0aa4.mp4"
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
