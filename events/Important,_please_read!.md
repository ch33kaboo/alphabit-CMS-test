https://media4.giphy.com/media/ZDFBmWibjnHwmYPv66/giphy.gif?cid=6c09b952a060a2f975ac678eb9e88785a618ba04868858c8&rid=giphy.gif&ct=ts

$$img-end$$

# Contribute & Write about an event / modify event content

If you are a member in AlphaBit Club, and you want to write about an event that you organized, you can contribute by writting about that in a MarkDown file from [here](https://github.com/ch33kaboo/alphabit-CMS-test/new/main/events). 
or If you find something mentioned that is wrong or inaccurate, modify that in [this repo](https://github.com/ch33kaboo/alphabit-cms-test) and make a PR.

# How to Contribute?

* visit [this link](https://github.com/ch33kaboo/alphabit-CMS-test/new/main/events).
* the name of your file should be the title of the blog, but you file name has to be in a certain structure:
  * Use underscores (_) instead of spaces.
  * The file name has to have `.md` file extention.
  * You should write all letter in lower case.
  * > **Example:** here is an example on how your file should be named: coding_challenge.md , startup_weekend.md ...
* The content of that file also has to be written in a certain structure:
  * The first line of your file must be the URL of the thumbnail image, like this one: ![thumbnail_image](https://i.postimg.cc/W3vc6TGg/thumbnail.png)
  * Then the second line of your file, has to be this string: `$$img-end$$` , this tells the CMS that the image URL is over.
  * Now, on the third and upcoming lines of your file, will be the content of your article, it has to be markdown.
  * > **Example:** For example, the words you're reading right now exist in a markdown file that was uploaded on the CMS repo, you can see its content from [here](https://github.com/ch33kaboo/CMS-test/blob/main/blog/Important%2C_please_read!).

### Recommendations:
* If you want to write code in your markdown, please avoid using the common method which is using Backticks, since the file content might get sanitized and the content will not render properly on the web page, instead use the `HTML code tag` .
* In your file, **do not dox or share any content that might be considered as inappropriate or offensive to a specific group of people** .
* Make sure that the information that you are providing about that specific event are valid, otherwise your PR will not be accepted.
