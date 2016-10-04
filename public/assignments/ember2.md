Ember 2
===

Create a new Ember application.

### 1. The artists Route

When a user visits /, the user should be redirected to the `artists` route (with the path /artists). This page should render a list of artists from the endpoint [http://itp-api.herokuapp.com/api/artists](http://itp-api.herokuapp.com/api/artists).

Each artist should be a link using the `link-to` helper to the `artists.artist` route, where the URL path is `/artists/:id`.

### 2. The artists.artist Route

The `artists.artist` route is a nested route that should fetch all the songs for the artist from the endpoint `http://itp-api.herokuapp.com/api/artists/:id/songs` where `:id` is the artist id. For example: [http://itp-api.herokuapp.com/api/artists/1/songs](http://itp-api.herokuapp.com/api/artists/1/songs).

At the top of this route's template, display the number of songs for this artist. Something like "This artist has X songs". Next, display all of the songs. Include the following song properties:

* title
* price
* playCount

### 3. The song-item Component

Instead of rendering each song on the `artists.artist` template, create a `song-item` component that receives a song and renders the songs details. For example:

```
{{song-item song=song}}
```

This component is responsible for rendering a single song object.

Next, if the song has a `playCount` greater than 20, somehow show the user that this song is popular using a computed property called `isPopular`. You can use an image, icons, CSS, etc. I'll leave the creativity up to you.

Similarly, create a computed property based on the price. If the price is less than $1.00, show one $. Otherwise, show $$.

Lastly, add a "Like" text button. The button should be gray initially. When the user clicks on this text button, it should turn blue. If the user clicks on the blue Like text button, it should turn back to gray. (Just like how it works on Facebook). Check out the "Like" icons from Font Awesome: [http://fontawesome.io/icons/](http://fontawesome.io/icons/)

### Submission

Just push your code up to GitHub under a repository called __exactly__ "itp404-assignment5".
