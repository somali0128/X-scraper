# Koii Twitter Crawler CLI

## Project Overview

The Koii Twitter Crawler is a sophisticated command-line interface (CLI) tool designed for ethical data gathering and archival of social media content. Built on the Koii network's task architecture, this tool enables community-driven content collection with a strong emphasis on responsible and legal usage.

### Key Features
- 🔍 Advanced Twitter search and data crawling
- 🌐 Decentralized task execution via Koii network
- 📊 Configurable search parameters
- 🔒 Ethical data gathering principles

### Use Cases
- Academic research and social media trend analysis
- Personal content archival
- Community-driven content preservation
- Open-source intelligence gathering (within legal boundaries)

## Installation

### Prerequisites
- Node.js (v14+ recommended)
- Yarn or npm
- Twitter Developer Account (optional, for advanced features)

### Install via npm
```bash
npm install -g koii-twitter-crawler
```

### Install via GitHub
```bash
git clone https://github.com/your-org/koii-twitter-crawler.git
cd koii-twitter-crawler
yarn install
```

## Usage

### Basic Search
```bash
# Search for tweets containing a specific hashtag
koii-crawler search --term "#koii" --limit 100
```

### Advanced Crawling
```bash
# Perform recursive crawling with custom depth
koii-crawler crawl \
  --term "web3" \
  --limit 500 \
  --depth 3 \
  --recursive true
```

### Configuration
Edit `twitter-task.js` to customize crawler behavior:

```javascript
let query = {
    limit: 100,         // Total records to return
    searchTerm: "#koii", // Keyword to search
    depth: 3,           // Recursive search depth
    recursive: true     // Enable recursive crawling
}
```

## Command Reference

| Command   | Description                     | Options                                   |
|-----------|--------------------------------|-------------------------------------------|
| `search`  | Basic tweet search             | `--term`, `--limit`, `--output`           |
| `crawl`   | Advanced recursive crawling    | `--term`, `--limit`, `--depth`, `--recursive` |
| `archive` | Store collected data           | `--format`, `--destination`               |

## Configuration Files

### `.env` Configuration
Create a `.env.sample` file in the project root:
```ini
TWITTER_API_KEY=your_api_key
TWITTER_API_SECRET=your_api_secret
```

## Deployment to Koii Network

### Build Task
```bash
yarn webpack  # Build task executable
npx @_koii/create-task-cli  # Deploy to Koii network
```

## Project Structure
- `index.js`: Main CLI entry point
- `twitter-task.js`: Core task implementation
- `adapters/twitter/twitter.js`: Twitter-specific adapter
- `tests/`: Comprehensive test suite

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push and submit a Pull Request

### Running Tests
```bash
yarn test
```

## Ethical Usage Guidelines

⚠️ **Important**: This tool is for legal and ethical data gathering only. 
- Do not use for unauthorized data collection
- Respect individual privacy
- Comply with Twitter's Terms of Service
- Consult legal professionals if unsure

## License

This project is licensed under the ISC License. See `LICENSE` file for details.

## Additional Resources
- [Koii Network Documentation](https://docs.koii.network)
- [Task Deployment Guide](https://blog.koii.network/How-to-deploy-a-koii-task-in-less-than-5mins/)

---

Built with ❤️ by the Koii Network Community