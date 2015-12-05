There are several optimizations were performed for the "news-aggregator" website:

In app.js:

1. Elimited looping all stories, instead the right story was chosen directly
2. Created storyDetails outside of onStoryClick method and assigned html to storyDetails without creating a new one all the time
3. Used CSS to slide in/out stories instead of javascript that triggered forced synchronous layout.
4. Got rid of setTimeout for animation, used requestAminationFrame instead.
5. Made visual changes in a requestAnimationFrame.
6. Removed colorizeAndScaleStories function as it gave little benefits, but triggers layout thrashing in the process.

In app.css:

1. Eliminated style recalculations when we bring a story in.
2. Eliminated double/triple shadows
3. Promote every child element in story-details
4. Added CSS to slide in/out stories


Assets for the news-aggregator website were taken from udacity.com website, Frontend Program. See folowing information:

# Udacity 60fps Course Samples

**Please note: this code is intended for you to hone your debugging skills. It contains a lot of code that you should not use in production!**

This is a simple web app that shows the top stories from [Hacker News](https://news.ycombinator.com/news) via [its API](http://blog.ycombinator.com/hacker-news-api).

Unfortunately it has a bunch of performance issues, such as:

* Layout Thrashing
* Expensive painting
* Unnecessary layouts
* Long-running and badly-timed JavaScript
* Bad touch handling

Your mission is to find and fix the issues, and make the app gloriously performant!

## License

See /LICENSE for more.

This is not a Google product.
