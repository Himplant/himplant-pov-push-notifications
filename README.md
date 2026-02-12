# Himplant Push Notifications Admin Panel

A simple web interface for sending push notifications to Himplant app users.

## 🚀 Features

- Send push notifications to all users
- Send notifications to yourself only (single email target)
- Send notifications to specific users (comma/newline separated emails)
- Optional filter: only users with incomplete questionnaire
- Real-time delivery status
- Clean, professional interface

## 📋 Usage

1. Open `index.html` in your browser
2. Fill in the notification details:
   - **Title**: Notification headline
   - **Message**: Notification body text
   - **Who should receive this**:
     - `Everyone`
     - `Me only` (requires your email)
     - `Specific users` (paste one or more user emails)
   - **Additional filter (optional)**: limit to users with incomplete questionnaire
3. Click "Send Notification"
4. View delivery results

## 🔧 Deployment to Vercel

### Option 1: Vercel CLI
```bash
cd admin-panel
npm install -g vercel
vercel --prod
```

### Option 2: GitHub + Vercel
1. Push this folder to a GitHub repository
2. Connect the repo to Vercel
3. Deploy automatically

## 🔒 Security Note

This admin panel uses Supabase anon key for authentication. For production use, consider:
- Adding user authentication
- Restricting access to authorized personnel
- Using environment variables for API keys

## 📱 How It Works

1. **Frontend**: HTML form collects notification details
2. **API Call**: Sends data to Supabase Edge Function
3. **Backend**: Edge Function queries user push tokens
4. **Delivery**: Expo Push Service sends notifications to devices

## 🆘 Support

For issues with the admin panel, check:
- Browser console for JavaScript errors
- Network tab for API request failures
- Supabase dashboard for function logs





