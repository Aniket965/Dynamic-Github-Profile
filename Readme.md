# Dynamic Github Profile
> Refresh this page to see different Images

![](https://bingimages.herokuapp.com/unsplash1)

# What?
we can  show dynamic Images on our github profile special repository ```githubhandle/githubhandle```
by creating an API which returns different images

example: 
> using unsplash random images
```md
https://source.unsplash.com/random/800x400
``` 
will show a random image like this

![](https://bingimages.herokuapp.com/unsplash2)

## Ideas
we can use this and create various different kind of profiles, some examples of that are: -
- Based on Time, we can create something like dynamic wallpapers in mac
- Based on Festivals, we can greet our profile visitor and make something special on special occasions
- Based on Birthdays, we can let our visitors know about our birthdays and create special effects on our profile
- Based on Daily Wallpapers or Quotes, you can show a daily quote on your github profile
- Based on News that you follow
- Based On random Thing that you like 
    - example ```https://source.unsplash.com/random/800x400?star ```
- Based on Your Latest Instagram post
# How? 
> for creating dynamic effect you have to host a server which returns your content

Code Snippet for creating route in Express.js
```js
app.get("/unsplash", (req, res) => {
  request("https://source.unsplash.com/random/800x200")
    .on("response", response => {
      response.headers['Cache-Control'] = 'max-age=0, no-cache, no-store, must-revalidate'
    })
    .pipe(res);
})
```
- **Note :-** set ```Cache-Control: max-age=0, no-cache, no-store, must-revalidate``` otherwise github will cache images for too long

### More Ideas? Contact Twitter - [@aniket965as](https://twitter.com/aniket965as)

