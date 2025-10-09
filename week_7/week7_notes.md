## Accessibility
> 'Web accessibility means that people with some type of disability can make use of WEB in the same conditions as the rest of the people. When we talk about web accessibility, we refer to a web design and development that allows these people to percieve, understand, navigate and interact with the WEB.'

- Nearly every country has acts and conventions in place to help inclusion, this also affects requirements for web design, it must comply to these acts

- ISO standarts for accesibility:
    - ISO 9241-171
    - ISO 9241-110
    - ISO 9241-11 to 17
    - ISO 17915
    - ISO 13407

- Key points:
    - Design interfaces to be percievable, operable, understandable and robust
    - Ensure consistent and clear use of color, contrast and font size
    - Provide alternatives for auditory and visual information
    - Ensure all functionality can be operated vie a keyboard
    - Make outputs accessible through text, audio and visual cues; provide text equivalents for non-text content
    - Create accessible user documentation and help systems
    - Allow user customization for font sizes, colors and input methids
    - Reguraly test and evaluate accessibility with people with disabilities
    - Ensure compatibility with assistive technologies (screen readers, magnifiers, alternative input devices)
    - Adhere to local and international accessibility laws and regulations.

- Screen readers:
    - Most OS's has built in screen readers:

- Accessibility for visually impaired people:
    - Use semantic HTML, as tagd help sreen readers to navigate
        ```
        tabindex="number" Sets tabbing sequence for keybaord
        ```
## Mobility

- Large navigation controls
    - Increase padding and font size to make it easier
- Use of highlighting
    - Keyover highlighting
- Color customization
- Advanced accessibility: ARIA  
    - Roles to describe the type of widget presented such as 'menu', 'slider' etc.
    - Roles to describe the structure of the web page, such as headings and regions
    - Properties to describe the state widgets are in, such as 'checked' for a checkbox or 'readonly' for most form controls
    - Properties to define live regions of a page that are likely to get updates
    - A way to provide keyboard navigation for the web objects and events such as those mentioned above

## Automatic accessibility testing tools
- Benefits:
    - Efficiency
    - Consistency
    - Can identify wide range of issues

- Common features and functionalities of automated accessibility tools
    - HTML validation with multiple levels
    - 

### AChecker
- Checks the URL or HTML for accessibility problems
> "AChecker is an automated accessibility checker used to evaluate the accessibility of HTML pages and help ensure they can be accessed by all individuals, including those with disabilities using assistive technologies to navigate the internet."

### Best practices
- Incorporate testing early and often
- Establish checkpoints for accessibility compliance
- Foster a culture of accessibility within team

## Rectifying accessibility issues
- Run AChecker
- Fix issue
- Run AChecker
- Rinse and repeat until complies with necessary level of accessibility