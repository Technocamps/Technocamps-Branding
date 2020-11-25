# Creating a new resource

1. ## Create
   - Create an empty post from:
   - Dev site: http://test.technocamps.com/wp-admin/post-new.php?post_type=x-portfolio
   - Live site: http://www.technocamps.com/wp-admin/post-new.php?post_type=x-portfolio
   - The portfolio post type is used for our normal resources and materials.
   - The standard "post" post type is used for news articles.
   - An example post can be seen here on the [testing](http://test.technocamps.com/en/resource/artificial-intelligence/) or [live](http://www.technocamps.com/en/resource/artificial-intelligence/) site.
   - Whilst you're editing, you can use `Ctrl + S` to save your changes without posting the material.

2. ## Naming
   - Insert your workshop title
   - Check the permalink below the title is appropriate and tweak as needed. Shorter is better

3. ## Tags and Categories
   - ### Tags
   	- Tags are used for the resource's topics
   	- You can include acronyms such as `AI` as well as `Artificial Intelligence`
   		- Example: `scratch`, `python`, `unplugged`, `computational thinking` etc.
   	- You can click the `most used tags` button to check what tags other people have been using
	- ###	Category
		- Categories are used for hierarchical organisation of our content.
	   - Multiple categories can be selected if appropriate
		- The categories can be for modules such as `Modules > CS101` and `Modules > C3`, or for groups of resources such as `Activity Packs > Primary Activity Packs`
		- For subcategories, use full names
			- Example: `Activity Packs > Primary Activity Packs`, NOT `Activity Packs > Primary`.
			- This makes them to work with in other places on the sight.
		- Add which learner level the material aimed at e.g. `School Level > Secondary > 11+`
		- If this workshops is also part of a programme, create and/or select that category as well.
			- If in doubt, ask.

5. ## Uploading content
	- This includes any slides, 
   - Scroll down to the `Attachments` section of the editor and select `Add new attachment`
	- Create an appropriate folder under `Resources` folder
		- Example: `Resources > Secondary > Artificial Intelligence > Cymraeg` or `Resources > Activity Packs > Primary > Greenfoot > English`
		- Look for the stacked folder icon to find the nested folders.
	- These folders are just used for back-end organisation, and will not affect the links on the front end.
	- Make sure your files have sensible names as these are what will be shown after the file is downloaded.
		- Example: `Secondary AI Workbook V2 - EN.pdf`
	- You can now open this new folder and drag and drop your resources in
	- The `Title` and `Caption` options are what will be displayed for each file attachments section. You can edit these as necessary without breaking links.
	- Once you have uploaded all of the files, select those you want to attach and click `Add selected attachments`

6. ## Featured image
   - Create a landscape preview image for the resource
   - Ideal resolution is 1200 x 628 or 1.91:1
   - Upload your the featured image to the **same folder** as the resources with with a name something like `workshop_name_thumbnail.png`
   - Attach featured image to the post.

7. ## Embedding content
	- Embedding PDF Slides
		- The main slides should be embedded at the bottom of the post
		- The code below can be added into your post by going into the `Text` editor rather than the `Visual` editor.
		- If you're only adding PDF slides, all you need to do is edit the url part of the `[pdfjs-viewer url="..."]` shortcode.
			<pre>[pdfjs-viewer url="<b>/wp-content/uploads/2020/11/AI_AI_Slides_En.pdf</b>"]</pre>
			- This link can found in the media library under the `File URL` or with the `Copy URL` button
			- Using the whole link will work, but using a relative link with just the part from the `/wp-content/...` onwards is better as it will not break with domain name changes.
		- Below is a full example of the code to add the PDFs in a tabbed container.
			- In the example here, we have an english and a cymraeg tab, which are set in the `href`s of the `li` elements and the `id`s of the `tab-pane` `div`s
			- The tab that you want to be shown first has the `active` class on the `li` and `tab-pane`
			- These `tab-pane` divs can also contain other content such as text and images. 
			```
			<ul class="nav nav-tabs">
				<li class="active"><a href="#english" data-toggle="tab">English</a></li>
				<li><a href="#cymraeg" data-toggle="tab">Cymraeg</a></li>
			</ul>
			<div class="tab-content">
				<div id="english" class="tab-pane fade in active">
					[pdfjs-viewer url="/wp-content/uploads/2020/11/AI_AI_Slides_En.pdf"]
				</div>
				<div id="cymraeg" class="tab-pane fade">
					[pdfjs-viewer url="/wp-content/uploads/2020/11/AI_AI_Slides_Cy.pdf"]
				</div>
			</div>
			```
	- If you are adding other tabs such as the multiple youtube video embeds in an Activity Pack, you can see the [Activity Pack Example](#activity-pack-example)
		- In the `li` list, the `href`s match the `id`s of the `tab-pane`s but with a "`#`" at the start.
			- Use spaces instead of spaces in these 
		- As with the English/Cymraeg tabs, you have to set which tab you want to start as active.
		- You can put anything you want as the title within the `>...</a>` part of the `<a>` tag in the `<li>`.
		- If you are embedding videos, you can use the `<iframe>` snippets below and all you have to change is the end part of the `src` property to match whatever your YouTube video's ID is.
			- e.g.: `src="https://www.youtube.com/embed/..."` 

9. ## Save, Check, double check, triple check, then `Publish`.

---

# Activity Pack Example
```
<ul class="nav nav-tabs">
  <li class="active"><a href="#introduction" data-toggle="tab">Introduction</a></li>
  <li><a href="#startup" data-toggle="tab">Startup</a></li>
  <li><a href="#movement" data-toggle="tab">Movement</a></li>
  <li><a href="#functionality" data-toggle="tab">Functionality</a></li>
  <li><a href="#counter" data-toggle="tab">Counter</a></li>
  <li><a href="#debugging" data-toggle="tab">Debugging</a></li>
  <li><a href="#challenge" data-toggle="tab">Challenge</a></li>
</ul>
<div class="tab-content">
  <div id="introduction" class="tab-pane fade in active">
    Follow along with this third video to learn how to get your actors to move. You will be shown two ways of moving. Random movement and user-controlled movement through the keyboard.
    <iframe
      src="https://www.youtube.com/embed/Yq70lALaYcM"
      width="650"
      height="365"
      frameborder="0"
      allowfullscreen="allowfullscreen"
    ></iframe>
  </div>
  <div id="startup" class="tab-pane fade">
    This video covers the startup you will need to set up your world and add a few actors into the world.
    <iframe
      src="https://www.youtube.com/embed/pBZ9BT2OuS4"
      width="650"
      height="365"
      frameborder="0"
      allowfullscreen="allowfullscreen"
    ></iframe>
  </div>
  <div id="movement" class="tab-pane fade">
    Follow along with this third video to learn how to get your actors to move. You will be shown two ways of moving. Random movement and user-controlled movement through the keyboard.
    <iframe
      src="https://www.youtube.com/embed/IB3CdyO369U"
      width="650"
      height="365"
      frameborder="0"
      allowfullscreen="allowfullscreen"
    ></iframe>
  </div>
  <div id="functionality" class="tab-pane fade">
    This fourth video covers functionality tasks. These include how to make another actor disappear when it collides with another actor. This allows us to make collectables/things to eat. We also cover how to play a sound when an actor collides or touches another actor.
    <iframe
      src="https://www.youtube.com/embed/GKuddHjs1y0"
      width="650"
      height="365"
      frameborder="0"
      allowfullscreen="allowfullscreen"
    ></iframe>
  </div>
  <div id="counter" class="tab-pane fade">
    Within this video, the task of adding a counter is covered. The video will show you how to add a counter to your Greenfoot world, along with explaining how to make the counter count up when an event happens.
    <iframe
      src="https://www.youtube.com/embed/Yq70lALaYcM"
      width="650"
      height="365"
      frameborder="0"
      allowfullscreen="allowfullscreen"
    ></iframe>
  </div>
  <div id="debugging" class="tab-pane fade">
    This video covers debugging. If at any stage you get stuck or are struggling take a look at this video to check if it is part of the common errors explained here.
    <iframe
      src="https://www.youtube.com/embed/0i7PSIOSyuE"
      width="650"
      height="365"
      frameborder="0"
      allowfullscreen="allowfullscreen"
    ></iframe>
  </div>
  <div id="challenge" class="tab-pane fade">
    Now try to complete the challenge task!
    <a class="button" tabindex="0" href="http://twitter.com/home?status=%40Technocamps%20%23TechnocampsOnline%20">Tweet</a> us a video/picture to let us know how you've been getting along for the chance to earn some extra bonus points!! Don't forget to tag <a tabindex="0" href="https://twitter.com/technocamps">@Technocamps</a> and use our hashtag <a tabindex="0" href="https://twitter.com/hashtag/TechnocampsOnline">#TechnocampsOnline</a>
	<img src="https://www.technocamps.com/storage/app/uploads/public/5e7/3ca/38b/5e73ca38be8c6857728630.png" alt="Resource"/>
  </div>
</div>
```