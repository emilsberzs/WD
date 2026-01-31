# Template engines and other presentation tecniques- Minimal template engine
- ![alt text](image.png)
## Template engine specification
### Basic template engine requirements
- Separate layout from code and data
    - Some (easy to design) template file
    - Some way to render the data into template
- Display variables - special tags
    - A layer on top of the HTML (as HTML on its own doesnt support variables)
    - HTML-like syntax
    - Need to be able to parse it easily
    - Special tags like:
        - <% myvariable %>
        - {{ myvariable }}
- Iterate over lists, something like:
    - {{#each my_list}}
    - {{ item }}
    - {{/#each}}
- Branching, along the lines of:
    - {{#if test_expression}}
    - // do this...
    - {{ item }}
    - {{ #else }}
    - //do this
- Automatic update
    - A nice to have: checking for data updates and automatic re-rendering


# Template engine implementation
## Variables and rendering
### Template engine class
- Class:
    - Specifiction, blueprint
- Object:
    - Instantioation in real world, code
- Constructor:
    - Special type of function then when we're turning class into a real thingm it's some code that gets run automatically
- **_See index.html and template.html for implementation_**

## Template control flow:iteration
- Summary (from video):
    - New #each tag
    - Specify an array of data
    - Extract tag contents
    - Insert data to template fragment
- See index2.html and template2.html

## Template control flow:branching
- Summary (from video):
    - New tags: #if, else
    - Extracting the conditional
    - Extracting the if and else blocks
    - Running the logic
    - If-only
- See index3.html and template3.html

## Template control: Automatic updating
- Checks when data updates and then reloads the template