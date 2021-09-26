## How the browser renders a website?

> Rendering includes --> Parsing, layout, painting etc

When we look at the High level flow, there are two parsers, one parse the html another parse the css
and then together they goto the render tree, where the dom structure gets created on the browser and then layout, where the positioning, other styling things happen and then the paint, which means put it out into the view

1. Parsing HTML

The parser will implicitly add the head tags, html tags if missing and then add self closing tags, and then quotes around the attributes, and knows how to deal with div and paragraph

Parsing Flow:

> Tokenizer

The tokenizer will look for the start tag and the closing tag and then tokenize them seperately each of the tags

> Parse Tree

Parse tree be like it starts from html tag --> head --> body , in body it finds p tag and whats inside it and other tags like div tag and whats inside it like text or image or list tags

Then the parse tree turns to DOM Tree, through this how the javascript crawls through the html tags, that is how we interact with the javascript in the page, they are called as DOM Elements

Certain times the parsing of html will stop, in moments like if there is a script tag it stops to fetch iot from the network and then execute that script and then again continue on the parsing. <link> and <style> can cause the parsing

We have always been said that put the script tag at the bottom, so the parse will be uninterepted so that the dom elements will be rendered without interuption, faster to render

2. CSS Parsing

Parsed based on the CSSOM, where it has CSSStylesheet --> CSSRules --> Selectors & Declaration --> css properties

> now Render Tree,

Where it is a combination of both DOM and CSSOM, combines the both object models and style resolution, this will show you the actual representation of what will show on the screen

Render tree is actually multiple tree, they are RenderObjects which renders the objects the node itself ie. the node elements, we refer it to as dom elements -> parent node, child node, then RenderStyles which renders the style to those node elements like beautifying them, then RenderLayers which renders them/ align them accordingly, positioned abosulte, whether it has z-index applied to it, then Line Boxes which looks how to text is wrapped, their line hight, font-size etc.

The head, script, title are not seen in the page and also the node element if it has been mentioned display:hidden wont be seen in the view

And then combine all the styles, the styles the browser which has it by default and the external files we link it and inline styles, style is about writing rules over that element

3. Layout

Recursive process includes traverse through the render tree --> positioning the nodes and their size --> laying out their children

Doing a font-size change will lead to re-layout the entire document, same with the browser size the loyout will be re-organized ie. re-layout happens

4. Paint

Takes all the information from the render tree and then paints it to the view, the process is a 12 phase processing
it creates layers from the RenderObjects, then position the nodes, the RenderLayer can containe multiple RenderObjects which denotes the Many to One Relationship

For each layer, bitmap will be generated and then uploaded to the GPU as a texture and those textures composites to form a final image that gets renders to the screen, like individual bits will be put together to form the picture

Inline CSS:
Speeds up the first time paint, first the text gets rendered, then the style gets renderd like font-size, background, images etc

The inline css will overwrite the rules which has been set in the external css file
