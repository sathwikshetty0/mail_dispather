# Mass Mail Dispatcher

A lightweight web application for sending emails to recipients specified in a CSV file.

## Features

- **Single Email Sending**: Sends an email to one recipient at a time
- **CSV Integration**: Import recipient email addresses from a CSV file
- **Email Validation**: Automatically validates email addresses before sending
- **Real-time Feedback**: Progress tracking and status notifications
- **Clean UI**: Modern, responsive interface

## Getting Started

### Prerequisites

- A web server to host the application
- An EmailJS account for sending emails
- A valid service ID and template ID from EmailJS

### Installation

1. Clone this repository or download the files:
   ```
   git clone https://github.com/sathwikshetty0/mail_dispather.git
   ```

2. Open `index.html` in a text editor and update the EmailJS configuration:
   ```javascript
   emailjs.init('YOUR_USER_ID'); // Replace with your EmailJS user ID
   ```

3. Update the service ID and template ID in the `sendEmailOnce` function:
   ```javascript
   emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
   ```

4. Upload all files to your web server or host through GitHub Pages.

## Usage

1. **Access the Application**: Open the application in your web browser.

2. **Fill Out the Form**:
   - Enter your email address in the "From" field
   - Type the email subject
   - Upload a CSV file containing recipient email addresses (one per line)
   - Compose your message

3. **Review Emails**: The application will display valid and invalid email addresses from your CSV.

4. **Send Email**: Click the "Send Email" button to send your message to the first valid email address in your list.

5. **Monitor Progress**: The application will show the sending progress and notify you when completed.

## CSV File Format

The CSV file should contain one email address per line:

```
recipient1@example.com
recipient2@example.com
recipient3@example.com
```

## Template Customization

To customize the EmailJS template:

1. Log in to your EmailJS account
2. Navigate to the "Email Templates" section
3. Create or edit a template with the following parameters:
   - `to_email`: Recipient's email address
   - `from_name`: Sender's email address
   - `subject`: Email subject
   - `message_html`: Email message content

## Technical Details

### Technologies Used

- **HTML5**: Structure of the application
- **CSS3**: Styling and animations
- **JavaScript**: Client-side functionality
- **EmailJS**: Email delivery service

### Key Components

- **File Parser**: Reads and validates email addresses from CSV files
- **Email Validator**: Ensures email addresses are properly formatted
- **UI Components**: Responsive interface with progress indicators
- **Notification System**: Toast notifications for success/error messages

## Troubleshooting

### Common Issues

1. **Emails Not Sending**:
   - Verify your EmailJS credentials
   - Check network connectivity
   - Ensure your template is correctly configured

2. **Invalid Emails**:
   - Review your CSV format
   - Check for spaces or special characters in email addresses

3. **Slow Performance**:
   - Large CSV files may take longer to process
   - Consider splitting large recipient lists into smaller files

## Security Considerations

- This application runs entirely on the client side
- Your EmailJS credentials are visible in the code
- Consider implementing server-side processing for production use
- Add rate limiting to prevent abuse

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [EmailJS](https://www.emailjs.com/) for email delivery
- [Feather Icons](https://feathericons.com/) for UI icons

## Future Improvements

- Multi-email sending capability
- Email scheduling
- Custom templates
- Analytics and reporting
- Email preview functionality

---

**Note**: This application is designed for demonstration purposes. For production use, consider implementing proper authentication, rate limiting, and server-side processing.