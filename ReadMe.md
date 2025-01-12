# Open in WhatsApp  

## Overview  
**Open in WhatsApp** is a lightweight web tool that allows users to quickly open WhatsApp chats with pre-filled messages. Simply input a phone number and a message, and with one click, the chat will open in WhatsApp.  

## Features  
- Quick and easy to use.  
- Automatically formats messages for WhatsApp.  
- Responsive and user-friendly interface.  

## Demo  
https://oiwa.vercel.app
[Visit Live Link](https://oiwa.vercel.app/)

## Getting Started  

### Prerequisites  
To use this project, ensure you have the following:  
- A modern web browser (e.g., Chrome, Firefox, Edge).  
- An internet connection.  

### Installation  
1. Clone the repository or download the files.  
    ```bash  
    git clone https://github.com/your-username/open-in-whatsapp.git  
    ```  
2. Open the `index.html` file in your browser.  

## Usage  
1. Enter the phone number in the input field, including the country code (e.g., +91 for India).  
2. Type your desired message in the text area.  
3. Click the "Open" button.  
4. A new tab will open with WhatsApp pre-filled with the phone number and message.  

## Code Highlights  

### Core Functionality  
The key functionality is implemented in the form submission handler:  
```javascript  
document.getElementById('open-in-WA-form').addEventListener('submit', function (event) {  
    event.preventDefault();  
    const phone = document.querySelector('[name="phone"]').value.trim();  
    const message = encodeURIComponent(document.querySelector('[name="message"]').value.trim());  
    if (phone && message) {  
        window.open(`https://wa.me/${phone}?text=${message}`, '_blank');  
        this.reset();  
    } else {  
        alert("Please fill out both fields!");  
    }  
});  
```
Responsive Design

The interface is designed with a minimal and responsive layout, making it accessible across devices.

Meta Information
	•	Author: G Rohit
	•	Website: https://grohit.com
	•	LinkedIn: G Rohit

License

This project is open-source and available under the MIT License.