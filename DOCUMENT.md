# Birthday Countdown Website - Documentation

## Description

This is an interactive birthday countdown website that creates an engaging and personalized experience leading up to a special birthday celebration. The website features a password-protected entry, a real-time countdown timer, and a progressive music playlist that unlocks songs as the birthday approaches.

### Key Features

- **Password Protection**: Secure access with a customizable password
- **Real-Time Countdown**: Live countdown timer showing days, hours, minutes, and seconds until the birthday
- **Progressive Song Unlocking**: 18 songs that unlock one by one as the countdown approaches zero
- **Music Player**: Full-featured music player supporting YouTube Music URLs with playlist management
- **Birthday Celebration**: Animated celebration screen with confetti, balloons, and sparkles when the countdown ends
- **Responsive Design**: Beautiful, modern UI with smooth animations and transitions

### Technical Details

- Built with **React 18** and **Vite** for fast development and optimized builds
- Uses **Framer Motion** for smooth animations and transitions
- Supports **YouTube Music** integration for audio playback
- Fully responsive design that works on desktop and mobile devices

---

## User Manual

### Getting Started

#### Accessing the Website

1. Open the website in your web browser
2. You will see a password-protected entry screen
3. Enter the correct password to unlock access
4. If the password is incorrect, you'll see an error message - try again

#### Password Screen

- **Title**: "Something Special Awaits... ⏳"
- **Input Field**: Enter the secret code/password
- **Unlock Button**: Click to submit and access the countdown
- The screen features animated elements to build anticipation

---

### Countdown Phase

Once authenticated, you'll see the main countdown screen with two main sections:

#### 1. Countdown Timer

The countdown displays the time remaining until the birthday in four units:
- **Days**: Full days remaining
- **Hours**: Hours remaining in the current day
- **Minutes**: Minutes remaining in the current hour
- **Seconds**: Seconds remaining in the current minute

The timer updates in real-time every second.

#### 2. Music Player Section

The music player appears below the countdown and provides access to the progressive song playlist.

##### Understanding Song Unlocking

- **18 Songs Total**: The playlist contains 18 songs
- **Unlocking Schedule**:
  - **First song** unlocks when less than 18 days remain
  - **Second song** unlocks when less than 17 days remain
  - **Third song** unlocks when less than 16 days remain
  - This pattern continues...
  - **17th song** unlocks when less than 2 days remain
  - **18th song** (final) unlocks on the birthday itself (when countdown reaches 0)

##### Music Player Interface

**Today's Song Section:**
- Shows the currently unlocked song (the most recently unlocked one)
- Displays song number and total count (e.g., "Song 5 of 18")
- Shows how many songs are unlocked (e.g., "5 unlocked")

**Playback Controls:**
- **▶️ Play/Pause Button**: Start or pause the current song
- **📅 Today's Song Button**: Switch back to today's song if you're playing a different one from the playlist
- **📝 Lyrics Button**: Toggle lyrics display (if lyrics are available for the song)

**Playlist Box:**
- Shows all 18 songs in the playlist
- **Unlocked songs**: Display with their number and title, clickable to play
- **Locked songs**: Show as "🔒 Locked" and are not clickable
- **Today's song**: Marked with a "Today" badge
- **Selected song**: Highlighted when playing from the playlist

**YouTube Music Integration:**
- Songs with YouTube Music URLs are embedded in an iframe player
- The player includes standard YouTube controls (play, pause, volume, etc.)
- Note: YouTube Music URLs require internet connection

**Lyrics Display:**
- If a song has lyrics, they can be displayed by clicking the lyrics button
- Lyrics appear in an expandable panel below the player
- Click the ✕ button to close the lyrics panel

##### Playing Songs

**To Play Today's Song:**
1. The player automatically loads today's song
2. Click the ▶️ button to start playback
3. For YouTube Music songs, the embedded player will start

**To Play a Different Unlocked Song:**
1. Scroll to the playlist box
2. Click on any unlocked song (not locked)
3. The song will start playing automatically
4. The player title changes to "🎵 Playing from Playlist"
5. Click the 📅 button to return to today's song

**Song Status Indicators:**
- **Today**: Badge on the current day's song
- **Selected**: Highlighted when playing from playlist
- **Locked**: 🔒 icon for songs not yet unlocked

---

### Birthday Celebration Phase

When the countdown reaches zero, the website automatically transitions to the birthday celebration screen.

#### Celebration Features

**Animated Elements:**
- **Confetti**: 50 colorful confetti pieces falling continuously
- **Balloons**: 12 animated balloons rising from the bottom
- **Sparkles**: 30 twinkling sparkles appearing randomly across the screen

**Celebration Content:**
- **Main Title**: "🎂 Happy Birthday! 🎂"
- **Birthday Person's Name**: Displayed prominently
- **Animated Cake**: A cake with a flickering candle
- **Birthday Message**: "Wishing you a day filled with happiness and a year filled with joy! 🎉"
- **Animated Emojis**: Row of celebratory emojis (🎈🎁🎊🎉🎂🍰) with bouncing animation
- **Wishes**: "May all your dreams come true! ✨"

**Music Player on Celebration:**
- All 18 songs are now unlocked and available
- You can play any song from the complete playlist
- The player shows "All songs unlocked!"

---

### Tips and Best Practices

1. **Internet Connection**: YouTube Music songs require an active internet connection
2. **Browser Compatibility**: Works best on modern browsers (Chrome, Firefox, Safari, Edge)
3. **Mobile Experience**: The website is fully responsive and works on mobile devices
4. **Song Selection**: You can switch between songs at any time - the player remembers your selection
5. **Lyrics**: Not all songs may have lyrics - the lyrics button only appears when lyrics are available
6. **Playlist Navigation**: Scroll through the playlist to see all songs, both unlocked and locked

---

### Troubleshooting

**Password Not Working:**
- Ensure you're entering the correct password (case-sensitive)
- Check for any extra spaces before or after the password
- Contact the website administrator if you've forgotten the password

**Songs Not Playing:**
- Check your internet connection (required for YouTube Music)
- Try refreshing the page
- Ensure your browser allows autoplay (some browsers block autoplay)

**Countdown Not Updating:**
- The countdown updates every second automatically
- If it appears frozen, try refreshing the page
- Ensure your device's date and time are correct

**Songs Not Unlocking:**
- Songs unlock based on the countdown timer
- The first song unlocks when less than 18 days remain
- Check the countdown to see when the next song will unlock

**YouTube Player Not Loading:**
- Ensure you have an active internet connection
- Check if YouTube is accessible in your region
- Try refreshing the page

---

### Customization (For Administrators)

The website can be customized by modifying the source code:

- **Password**: Change `PASSWORD` constant in `App.jsx`
- **Birthday Person Name**: Change `BIRTHDAY_PERSON` constant
- **Target Date**: Modify `getTargetDate()` function (currently set to November 27th)
- **Songs**: Edit the `SONGS_LIST` array to add/remove songs
- **Styling**: Modify `App.css` for visual customization

---

## Technical Specifications

- **Framework**: React 18.2.0
- **Build Tool**: Vite 5.0.8
- **Animation Library**: Framer Motion 12.23.24
- **Styling**: CSS with Tailwind CSS 4.1.17
- **Music Integration**: YouTube Music API (embedded iframe)

---

## Support

For technical issues or questions about the website, please contact the website administrator or refer to the project's README.md file for development setup instructions.

---

*Last Updated: 2024*

