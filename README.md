<<<<<<< HEAD
# PartyHub - Instagram Event Aggregator

This project extracts and displays upcoming events from multiple Instagram accounts, showing them on a web dashboard with links to the original Instagram posts.

## Features

- **Automatic Event Extraction:**
  - Every time the site is accessed, the event extractor runs (if the data is older than 30 minutes) and updates the event data from Instagram.
- **Multi-Account Support:**
  - Extracts events from multiple Instagram accounts, including: `blackout.cal`, `overhype.ccu`, `iammissginko`, `vybe.cal`, `mbarkitchen`, and `thenewmadamg`.
- **Duplicate Event Merging:**
  - Events containing both "karaoke" and "wednesday" in their name or caption are merged into a single event, combining all sources.
- **Instagram Post Links:**
  - Each event card includes a "Click here for the ig post" link to the original Instagram post.
- **Modern UI:**
  - Events are displayed in a visually appealing card format.
- **Caching:**
  - The extractor only runs if the data is older than 30 minutes, for fast page loads and to avoid API rate limits.

## Prerequisites

1. **Scrape.do API Token:**
   - Sign up at [https://scrape.do](https://scrape.do) and get your API token.
2. **Python Dependencies:**
   - Install required packages:
     ```bash
     pip install -r requirements.txt
     ```

## Usage

1. **Configure Instagram Accounts:**
   - Edit the `USERNAMES` list in `multi_account_event_extractor.py` to add or remove Instagram accounts.
2. **Run the Flask App:**
   ```bash
   python app.py
   ```
3. **View in Browser:**
   - Open [http://localhost:5000](http://localhost:5000) to see the latest events.

## How It Works

- When a user visits the site, the backend checks if the event data is older than 30 minutes.
- If so, it runs `multi_account_event_extractor.py` to fetch and process the latest events from all configured Instagram accounts.
- Events are parsed, merged (if needed), and displayed on the site, including direct links to the Instagram posts.

## Output Files

- `multi_account_events.json`: Structured JSON data with all event information.
- `multi_account_events.txt`: Human-readable text file with event details and Instagram post links.

## Customization

- **Change Update Interval:**
  - Edit `UPDATE_INTERVAL_SECONDS` in `app.py` (default: 1800 seconds = 30 minutes).
- **Change Merging Logic:**
  - Update the `remove_duplicate_events` method in `multi_account_event_extractor.py` to merge events based on your own criteria.

## Legal Considerations

- This script is for educational and research purposes.
- Only scrape public Instagram accounts.
- Respect Instagram's Terms of Service and Scrape.do's usage policies.

---

For questions or contributions, open an issue or pull request! 
=======
# PartyHub
One-stop Flask-based web app to view all party events happening in Kolkata — scraped directly from Instagram.
>>>>>>> b87ec6fa926e7e06edd7f782b34ac183dc0e5307
