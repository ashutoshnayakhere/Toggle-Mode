# Toggle-Mode

![Capturenn](https://github.com/user-attachments/assets/c518344c-fd0e-4ca1-acab-6578f37a836d)
![image](https://github.com/user-attachments/assets/1cefb6d6-7242-4b7b-b54e-c3c121b758ee)


### Documentation for Night/Day Mode Toggle Code

---

#### **HTML Structure**

1. **DOCTYPE Declaration**: 
   The document begins with the `<!DOCTYPE html>` declaration, defining that the document is an HTML5 document.

2. **`<html>` Tag**:
   The root element of the HTML document, it contains the `lang` attribute specifying the language as English (`en`).

3. **`<head>` Section**:
   - **Meta Tags**: 
     - `<meta charset="UTF-8">` specifies the character encoding as UTF-8.
     - `<meta name="viewport" content="width=device-width, initial-scale=1.0">` ensures the page is responsive and scales appropriately on different devices.
   - **Title**: 
     The title of the page is set using `<title>Document</title>`.

4. **`<style>` Section**:
   The CSS for the page is included in this section to style the elements like the body, night/day mode toggle button, and optional flexbox layout.

#### **CSS Styling**

1. **Body**:
   - `transition: 1.5s;`: Adds a smooth transition effect of 1.5 seconds to any changes made to the body's style, such as background color changes during the toggle.

2. **Night Toggle Button (`.night-toggle`)**:
   - Defines the toggle button size (33px by 33px) and its position on the screen (absolute, top-right).

3. **Hover Effect (`.night-toggle:hover`)**:
   - Changes the cursor to a pointer when hovering over the toggle button, indicating it is clickable.

4. **Moon Icon (`.moon`)**:
   - Represents the moon during day mode. It is styled with a bluish shadow and border to give a moon-like appearance. The icon has smooth transitions (2 seconds) for visual changes.

5. **Sun Icon (`.sun`)**:
   - Represents the sun during night mode. It has a yellow background and a shadow to resemble the sun. Like the moon, it transitions smoothly between states.

6. **Optional Content Styling**:
   - **`.opt`**: A flexbox container is used to center and align content with some margins.
   - **`.break`**: A utility to provide space between flexbox items.

#### **Body Content**

1. **Night Toggle**:
   - A `div` element with the class `night-toggle` is used as a button to toggle between night and day mode. Inside it is a `div` with the id `moon`, which represents the current state (moon or sun).

2. **Optional Flexbox Content**:
   - A `div` with the class `opt` contains an `h1` header and some instructional `p` elements to guide the user on how to use the toggle button.

#### **JavaScript**

1. **`switchMode()` Function**:
   - This function is triggered when the user clicks the toggle button.
   
   - **Moon to Sun Transition**:
     When the `moon` class is present, it switches the class to `sun`. This causes the body background color to change to dark (`#141D26`) with white text, simulating night mode.

   - **Sun to Moon Transition**:
     When the class is `sun`, it switches back to `moon`, changing the background color to white and the text color to black, simulating day mode.

2. **Class Toggle Mechanism**:
   - The class toggling mechanism relies on checking the current class of the moon/sun div (`if(moon.className=="moon")`), and then switching it to either sun or moon.

#### **How It Works**

- By clicking the moon icon (located at the top right), the user can toggle between day mode (white background, black text) and night mode (dark background, white text). The `moon` div changes its appearance to resemble the sun or moon based on the mode, and the background color transitions smoothly.

#### **Enhancements**
- You could add local storage functionality to save the user's preference for night or day mode even after they leave the page.

--- 

This document provides a detailed explanation of how the code implements a day/night mode toggle feature using HTML, CSS, and JavaScript.
