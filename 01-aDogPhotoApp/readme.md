#  Notes of Learning Basic HTML by a Dog Photo App
[TOC]
## basic framework
```html
<!--All pages should begin with <!DOCTYPE html>. This special string is known as a declaration and ensures the browser tries to meet industry-wide specifications.-->
<!DOCTYPE html>
<!-- HTML5 has some elements that identify different content areas. These elements make your HTML easier to read and help with Search Engine Optimization (SEO) and accessibility. -->
<!--Notice that the entire contents of the page are nested within an html element. All other elements must be descendants of this html element.-->
<!--Add the lang attribute with the value en to the opening html tag to specify that the language of the page is English.-->
<html lang="en">
<!--HTML attributes are special words used inside the opening tag of an element to control the element's behavior.-->
<!-- Other important information goes inside the head element.-->
<head>
<!--The title element determines what browsers show in the title bar or tab for the page.-->
	<title></title>
	<!--One more thing. You should allow people to use their native language. Tell the browser to encode multiple languages by adding a meta element as a child of the head element. Set its charset attribute to UTF-8.-->
	<meta charset="utf-8">
</head>
<!--All page content elements that should be rendered to the page go inside the body element. -->
<body>
	<!--Identify the main section-->
	<main>
		<!--section element: to separate this content from the future content.-->
		<section></section>
		<section></section>
	</main>
	<footer>
	</footer>
</body>
</html>
```
##codes with comments
```html
<!DOCTYPE html>

<html lang="en">
<head>
	<title>DogPhotoApp</title>
</head>
<body>
<!--The h1 to h6 heading elements are used to signify the importance of content below them. The lower the number, the higher the importance, so h2 elements have less importance than h1 elements. Only use one h1 element per page and place lower importance headings below higher importance headings.-->
	<h1>DogPhotoApp</h1>
	<main>
		<section>
			<h2>Dog Photos</h2>
			<!--The p element is used to create a paragraph of text on websites. -->
			<!--You can link to another page with the anchor (a) element. -->
			<!--Add a target attribute with the value _blank to the anchor (a) element's opening tag, so that the link opens in a new tab.-->
			<p>Click here to view more <a target="_blank" href="default.html" >dog photos</a>.</p>
			<!--You can add images to your website by using the img element. img elements have an opening tag without a closing tag. A tag for an element without a closing tag is known as a self-closing tag.-->
			<!--HTML attributes are special words used inside the opening tag of an element to control the element's behavior. The src attribute in an img element specifies the image's URL (where the image is located).-->
			<!--All img elements should have an alt attribute. The alt attribute's text is used for screen readers to improve accessibility and is displayed if the image fails to load.-->
			<!--Turn the image into a link by surrounding it with necessary element tags. -->
			<a target="_blank" href="default.html"><img src="img/cute dog.jpg" alt="A cute dog"></a>
		</section>
		<section>
			<h2>Dog lists</h2>
			<!--When you add a lower rank heading element to the page, it's implied that you're starting a new subsection.-->
			<h3>Things dogs love:</h3>
			<!--Unordered list (ul) element. Note that nothing will be displayed at this point.-->
			<ul>
			<!--Use list item (li) elements to create items in a list. -->
				<li>exploring</li>
				<li>running</li>
				<li>balls</li>
			</ul>
			<!--The figure element represents self-contained content and will allow you to associate an image with a caption.-->
			<figure>
				<img src="img/The dog is playing a ball.jpg" alt="The dog is playing a ball.">
				<!--A figure caption (figcaption) element is used to add a caption to describe the image contained within the figure element.-->
				<!--em element: to Emphasize the word .-->
				<figcaption>Dogs <em>love</em> balls.</figcaption>
			</figure>
			<h3>Top 3 things dogs hate:</h3>
			<!--Ordered list (ol)  element. List items in an ordered list are numbered when displayed.-->
			<ol>
				<li>Being Left On Their Own</li>
				<li>Scary Fireworks</li>
				<li>Being Bored</li>
			</ol>
			<figure>
				<img src="img/An angry dog.png" alt="An angry dog.">
				<!--The strong element is used to indicate that some text is of strong importance or urgent.-->
				<figcaption>An <strong>angry</strong> dog.</figcaption>
			</figure>
		</section>
		<section>
			<h2>Dog Form</h2>
			<!--A web form to collect information from users.-->
			<!--The action attribute indicates where form data should be sent. For example, <form action="/submit-url"></form> tells the browser that the form data should be sent to the path /submit-url.-->
			<form action="default.html">
			<!--The fieldset element is used to group related inputs and labels together in a web form. fieldset elements are block-level elements, meaning that they appear on a new line.-->
				<fieldset>
				<!--The legend element acts as a caption for the content in the fieldset element. It gives users context about what they should enter into that part of the form.-->
					<legend>Is your dog an indoor or outdoor dog?</legend>
					<!--The input element allows you several ways to collect data from a web form. Input elements are self-closing.There are many kinds of inputs you can create using the type attribute. You can easily create a password field, reset button, or a control to let users select a file from their computer. -->
					<!--In order for a form's data to be accessed by the location specified in the action attribute, you must give the text field a name attribute and assign it a value to represent the data being submitted. For example, you could use the following syntax for an email address text field: <input type="text" name="email">.-->
					<!--To prevent a user from submitting your form when required information is missing, you need to add the required attribute to an input element. There's no need to set a value to the required attribute. Instead, just add the word required to the input element, making sure there is space between it and other attributes.-->
					<!--You can use radio buttons for questions where you want only one answer out of multiple options.-->
					<!--label elements are used to help associate the text for an input element with the input element itself (especially for assistive technologies like screen readers).-->
					<!--The id attribute is used to identify specific HTML elements. Each id attribute's value must be unique from all other id values for the entire page.-->
					<!--Notice that both radio buttons can be selected at the same time. To make it so selecting one radio button automatically deselects the other, both buttons must have a name attribute with the same value.-->
					<!--If you select the Indoor radio button and submit the form, the form data for the button is based on its name and value attributes. Since your radio buttons do not have a value attribute, the form data will include indoor-outdoor=on, which is not useful when you have multiple buttons.-->
					<label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" >indoor</label>
					<label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor" >outdoor</label>
				</fieldset>
				<fieldset>
					<legend>What's your dog's personality?</legend>
					<!--Forms commonly use checkboxes for questions that may have more than one answer. -->
					<!--There's another way to associate an input element's text with the element itself. You can nest the text within a label element and add a for attribute with the same value as the input element's id attribute.-->
					<!--In order to make a checkbox checked or radio button selected by default, you need to add the checked attribute to it. There's no need to set a value to the checked attribute. Instead, just add the word checked to the input element, making sure there is space between it and other attributes.-->
					<input id="loving" type="checkbox" name="personality" value="loving" checked><label for="loving">Loving</label>
					<input id="lazy" type="checkbox" name="personality" value="lazy" checked><label for="lazy">Lazy</label> 
					<input id="energetic" type="checkbox" name="personality" value="energetic" checked><label for="energetic">Energetic</label>
				</fieldset>
				<input type="text" name="dogphotourl" placeholder="dog photo URL" required>
				<!--Both input and button elements are inline elements, which don't appear on new lines.-->
				<button type="submit">Submit</button>
			</form>
		</section>
	</main>
	<footer>
		<p>No Copyright - <a href="A Dog Photo App.html">yuzhencode</a></p>
	</footer>
</body>
</html>
```
