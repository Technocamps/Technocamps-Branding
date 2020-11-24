# Creating a new resource

1. ## Create
   - Create an empty post from:
   - Dev site: http://test.technocamps.com/wp-admin/post-new.php?post_type=x-portfolio
   - Live site: http://www.technocamps.com/wp-admin/post-new.php?post_type=x-portfolio
   - The portfolio post type is used for our normal resources and materials
   - The standard "post" post type is used for news articles.

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
	- The main slides should be embedded

```
Artificial Intelligence (AI) is the intelligence exhibited by machines or software, and there are many interesting questions around this topic. Can you program a computer to think?

This workshop uses a selection of online tools such as chatbots to analyse these questions and to give students an understanding of Artificial Intelligence

Are computers intelligent or not? Looking at online tools such as ChatBots, including “Turi” developed by Aberystwyth University, helps us look at Turing’s work on the intelligence of machines.

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

9. Save and check, double check, tripple check.
