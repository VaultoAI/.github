# Vaulto AI - Comprehensive Platform Documentation

<div align="center">

![Vaulto AI](https://img.shields.io/badge/Vaulto-AI-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

**Building the world's most secure stablecoin and private investing infrastructure for the future of finance**

[Website](https://www.vaulto.ai) • [Documentation](https://docs.vaulto.ai) • [Support](mailto:support@vaulto.ai)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Platform Components](#platform-components)
  - [Vaulto Search](#vaulto-search)
  - [Vaulto Swap](#vaulto-swap)
  - [Vaulto Holdings](#vaulto-holdings)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Technology Stack](#technology-stack)
- [Security & Compliance](#security--compliance)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Support](#support)

---

## Overview

**Vaulto AI** is a pioneering platform at the intersection of artificial intelligence and decentralized finance (DeFi). By leveraging AI-driven infrastructure, Vaulto seamlessly connects information, assets, and capital with intelligent automation and tokenized real-world solutions.

### Core Mission

Vaulto AI is dedicated to building secure, compliant, and intelligent infrastructure for managing digital assets. Our platform empowers users to navigate the evolving financial landscape with confidence through:

- **AI-Powered Analytics**: Real-time market insights and intelligent investment guidance
- **Decentralized Trading**: MEV-protected asset swapping across multiple blockchain networks
- **Institutional Tools**: Professional-grade dashboards and portfolio management solutions

### Key Features

**Multi-Chain Support** - Ethereum, Arbitrum, Optimism, Base, and Polygon  
**MEV Protection** - CoW Protocol integration prevents front-running  
**AI-Driven Insights** - Real-time market analysis and recommendations  
**Professional Dashboards** - Institutional-grade analytics and reporting  
**Secure Authentication** - WalletConnect integration with SIWE standards  
**Institutional Solutions** - Custom limits, treasury tools, and APIs  

---

## Platform Components

### Vaulto Search

**AI-Powered Market Intelligence & Analytics Platform**

Vaulto Search is an advanced analytics and search tool that provides real-time market insights, comprehensive data analysis, and intelligent investment guidance through an integrated dashboard interface.

#### Key Features

- **Real-Time Analytics Dashboard**
  - Comprehensive analytics file management system
  - Google Drive integration for document storage and retrieval
  - Organized analytics by category (Landing, Search, Swap)
  - Real-time file synchronization and updates

- **Intelligent Search Capabilities**
  - Advanced search functionality across analytics data
  - Filter and categorize analytics files
  - Quick access to historical data and reports
  - Export and sharing capabilities

- **Market Intelligence**
  - Real-time market data aggregation
  - Performance metrics and trend analysis
  - Customizable analytics views
  - Data visualization tools

- **Secure Access**
  - WalletConnect authentication integration
  - SIWE (Sign-In with Ethereum) standard compliance
  - Server-side signature verification
  - Session management with secure HTTP-only cookies

#### Technical Implementation

- **Framework**: Next.js 16 with App Router
- **Authentication**: WalletConnect v2 with Reown AppKit
- **Storage**: Google Drive API integration
- **Security**: Iron-session for secure session management
- **Database**: PostgreSQL with Drizzle ORM

#### Use Cases

- **Market Research**: Access comprehensive market analytics and reports
- **Performance Tracking**: Monitor portfolio and asset performance metrics
- **Data Analysis**: Analyze historical trends and patterns
- **Reporting**: Generate and share custom analytics reports

#### Repository

- **GitHub**: [vaulto-dev](https://github.com/charlie-818/vaulto-dev)
- **Live Dashboard**: Available through authenticated access

---

### Vaulto Swap

**Permissionless DeFi Protocol for Real World Asset (RWA) Trading**

Vaulto Swap is a decentralized exchange protocol that enables seamless swapping of tokenized Real World Assets (RWAs) across multiple EVM-compatible blockchains. Built on CoW Swap's MEV-protected batch auction engine, it provides optimal execution and settlement for RWA trades.

#### Key Features

- **Multi-Chain RWA Trading**
  - Trade tokenized US Treasuries, equities, commodities, and ETFs
  - Support for Ethereum, Arbitrum, Optimism, Base, and Polygon
  - Cross-chain asset accessibility
  - Unified trading interface across networks

- **MEV Protection**
  - CoW Protocol integration prevents front-running
  - Protection against sandwich attacks
  - Batch auction execution for optimal pricing
  - Intent-based trading system

- **Asset Support**
  - **xStocks**: 60+ tokenized stocks (TSLAx, AAPLx, GOOGLx, AMZNx, MSFTx, etc.)
  - **Stablecoins**: USDC, USDT, DAI
  - **Crypto Assets**: WBTC, WETH
  - **RWAs**: Tokenized commodities, treasuries, and ETFs

- **Instant Execution**
  - Real-time price updates (10-second refresh)
  - Price impact calculation
  - Slippage protection
  - Fast transaction settlement

- **Mobile-First Design**
  - Responsive interface optimized for all devices
  - Touch-optimized controls
  - Sleek, modern UI with smooth animations
  - Professional user experience

#### Technical Implementation

- **Framework**: Next.js 14 with TypeScript
- **Trading Engine**: CoW Swap Widget integration
- **Web3**: Wagmi & Viem for Ethereum interactions
- **Wallet**: WalletConnect v2 support
- **Styling**: Tailwind CSS with custom design system
- **Charts**: Lightweight Charts for price visualization

#### Supported Networks

| Network | Chain ID | Status |
|---------|----------|--------|
| Ethereum | 1 | Active |
| Arbitrum | 42161 | Active |
| Optimism | 10 | Active |
| Base | 8453 | Active |
| Polygon | 137 | Active |

#### Use Cases

- **Portfolio Diversification**: Access traditional assets on-chain
- **Yield Generation**: Trade RWAs for passive income opportunities
- **Arbitrage**: Exploit price differences across chains
- **Institutional Trading**: Professional-grade RWA trading infrastructure

#### Repository

- **GitHub**: [Vaulto-Swap](https://github.com/charlie-818/Vaulto-Swap)
- **Live Application**: [app.vaulto.ai](https://app.vaulto.ai)

---

### Vaulto Holdings

**Professional Ethereum Vault Dashboard & Analytics Platform**

Vaulto Holdings provides institutional-grade solutions for managing digital assets, featuring a comprehensive dashboard that delivers real-time leverage, exposure, and performance metrics for Ethereum vault operations.

#### Key Features

- **Real-Time Metrics Dashboard**
  - **ETH Net Exposure**: Real-time leveraged exposure tracking with daily change indicators
  - **Total Leverage**: Current leverage ratio with daily and weekly change tracking
  - **Liquidation Price**: Risk monitoring with visual danger zone indicators
  - **Vault NAV**: Net Asset Value in both USD and ETH with performance tracking
  - **Total Vault Value**: Complete portfolio value overview

- **Performance Analytics**
  - **Ethereum Price Performance**: Real-time ETH price chart with 365-day historical data
  - **Daily/30-Day Returns**: Short-term performance metrics
  - **Real-time ETH Price Feed**: Live price updates from CoinGecko API
  - **Historical Charts**: Interactive price visualization with Recharts

- **Risk Management**
  - **Volatility Metrics**: 30-day and 1-year volatility tracking
  - **VaR (Value at Risk)**: 95% and 99% confidence intervals
  - **Open Interest**: Position monitoring and tracking
  - **Liquidation Risk**: Real-time distance from liquidation price calculations

- **Professional Design**
  - **MicroStrategy-inspired**: Clean, data-forward design aesthetic
  - **Responsive Layout**: Optimized for desktop and mobile devices
  - **Real-time Updates**: Auto-refreshing data with timestamps
  - **Data Source Attribution**: Clear citation of all data sources

#### Technical Implementation

- **Framework**: React 18 with TypeScript
- **Styling**: CSS3 with CSS Custom Properties
- **Charts**: Recharts for data visualization
- **Animations**: Framer Motion for smooth interactions
- **Data API**: CoinGecko API integration
- **HTTP Client**: Axios with retry logic
- **Routing**: React Router for navigation

#### API Integration

- **CoinGecko Integration**
  - Real-time ETH & BTC price feeds
  - Daily change percentage calculations
  - Batch API requests for efficiency
  - Automatic retry logic (3 attempts with exponential backoff)
  - Smart caching (60-second cache duration)
  - Manual refresh capabilities
  - Historical price data (365-day charts)
  - Graceful fallback to mock data

#### Data Sources

- **CoinGecko**: Primary source for ETH price data and historical charts
- **Hyperliquid**: Vault data and positions (planned integration)
- **Chainlink**: Price feeds and oracles (planned integration)

#### Use Cases

- **Institutional Portfolio Management**: Comprehensive vault monitoring and analytics
- **Risk Assessment**: Real-time risk metrics and liquidation monitoring
- **Performance Tracking**: Historical performance analysis and reporting
- **Compliance Reporting**: Data-driven reporting for regulatory compliance

#### Repository

- **GitHub**: [vaulto-holdings](https://github.com/charlie-818/vaulto-holdings)
- **Live Dashboard**: [vaulto-holdings.netlify.app](https://vaulto-holdings.netlify.app)

---

## Architecture

### System Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    Vaulto AI Platform                       │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │ Vaulto Search│  │ Vaulto Swap  │  │Vaulto Holdings│     │
│  │              │  │              │  │              │      │
│  │ • Analytics  │  │ • RWA Trading│  │ • Vault Metrics│    │
│  │ • Market Data│  │ • MEV Protect│  │ • Risk Mgmt   │      │
│  │ • AI Insights│  │ • Multi-Chain│  │ • Performance │      │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘      │
│         │                  │                  │              │
│         └──────────────────┼──────────────────┘             │
│                            │                                │
│         ┌──────────────────▼──────────────────┐            │
│         │     Shared Infrastructure            │            │
│         │  • WalletConnect Authentication     │            │
│         │  • Multi-Chain Support              │            │
│         │  • Security & Compliance            │            │
│         └─────────────────────────────────────┘            │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Component Integration

- **Shared Authentication**: All components use WalletConnect v2 for secure wallet connections
- **Multi-Chain Support**: Unified infrastructure across Ethereum and L2 networks
- **Data Aggregation**: Centralized data sources with component-specific APIs
- **Security Layer**: Consistent security standards across all platforms

---

## Getting Started

### Prerequisites

- **Node.js**: 18+ (20+ recommended)
- **npm**: 9+ or yarn
- **Git**: Latest version
- **Web3 Wallet**: MetaMask, Coinbase Wallet, or WalletConnect-compatible wallet

### Quick Start Guide

#### 1. Vaulto Search Setup

```bash
# Clone the repository
git clone https://github.com/charlie-818/vaulto-dev.git
cd vaulto-dev

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Add your WalletConnect Project ID and other required variables

# Set up database
npm run db:push

# Run development server
npm run dev
```

#### 2. Vaulto Swap Setup

```bash
# Clone the repository
git clone https://github.com/charlie-818/Vaulto-Swap.git
cd Vaulto-Swap

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Add NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID

# Run development server
npm run dev
```

#### 3. Vaulto Holdings Setup

```bash
# Clone the repository
git clone https://github.com/charlie-818/vaulto-holdings.git
cd vaulto-holdings

# Install dependencies
npm install

# Run development server
npm start
```

### Environment Variables

#### Vaulto Search (vaulto-dev)
```env
NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=your_project_id
SESSION_SECRET=your_secure_session_secret
POSTGRES_URL=your_postgres_connection_string
GOOGLE_DRIVE_API_KEY=your_google_api_key
GOOGLE_DRIVE_FOLDER_SEARCH=your_folder_id
```

#### Vaulto Swap
```env
NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=your_project_id
```

#### Vaulto Holdings
```env
# No environment variables required for basic setup
# CoinGecko API is used without authentication
```

---

## Technology Stack

### Frontend Technologies

| Component | Framework | Language | Styling |
|-----------|-----------|----------|---------|
| **Vaulto Search** | Next.js 16 | TypeScript | Tailwind CSS |
| **Vaulto Swap** | Next.js 14 | TypeScript | Tailwind CSS |
| **Vaulto Holdings** | React 18 | TypeScript | CSS3 |

### Blockchain & Web3

- **Ethers.js** v6 - Ethereum interaction library
- **Viem** v2 - TypeScript Ethereum library
- **Wagmi** v2 - React hooks for Ethereum
- **WalletConnect** v2 - Multi-wallet connection protocol
- **SIWE** - Sign-In with Ethereum standard

### Data & APIs

- **CoinGecko API** - Cryptocurrency price data
- **Google Drive API** - Analytics file storage
- **CoW Protocol** - MEV-protected trading
- **Hyperliquid** - Vault data (planned)

### Infrastructure

- **PostgreSQL** - Database (Vaulto Search)
- **Drizzle ORM** - Database toolkit
- **Netlify** - Hosting and deployment
- **Vercel** - Alternative hosting option

---

## Security & Compliance

### Security Features

**Multi-Layer Authentication**
- WalletConnect v2 integration
- SIWE (Sign-In with Ethereum) standard
- Server-side signature verification
- Secure session management with HTTP-only cookies

**MEV Protection**
- CoW Protocol integration prevents front-running
- Batch auction execution
- Intent-based trading system

**Data Security**
- Encrypted wallet creation
- Secure key storage recommendations
- Non-custodial architecture
- Server-side validation

### Compliance

- **KYC/AML**: Integrated compliance infrastructure
- **Transparent Audits**: Regular security audits
- **Asset-Backed**: Fully collateralized stablecoins
- **Regulatory**: Compliance with applicable regulations

### Best Practices

- Always verify contract addresses before transactions
- Use hardware wallets for large amounts
- Keep private keys secure and never share them
- Review transaction details before confirming
- Stay informed about platform updates and security notices

---

## Deployment

### Vaulto Search

**Netlify Deployment**
```bash
# Build command
npm run build

# Publish directory
.next
```

**Environment Variables Required:**
- `NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID`
- `SESSION_SECRET`
- `POSTGRES_URL`
- `GOOGLE_DRIVE_API_KEY`

### Vaulto Swap

**Vercel/Netlify Deployment**
```bash
# Build command
npm run build

# Publish directory
.next
```

**Environment Variables Required:**
- `NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID`

### Vaulto Holdings

**Netlify Deployment**
```bash
# Build command
npm run build

# Publish directory
build
```

**No environment variables required** for basic deployment.

---

## Contributing

We welcome contributions to the Vaulto AI platform! Please follow these guidelines:

### Development Workflow

1. **Fork the Repository**
   ```bash
   git clone https://github.com/vaulto-ai/[repository-name].git
   ```

2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make Your Changes**
   - Follow the existing code style
   - Add tests if applicable
   - Update documentation as needed

4. **Commit Your Changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```

5. **Push to Branch**
   ```bash
   git push origin feature/amazing-feature
   ```

6. **Open a Pull Request**
   - Provide a clear description of changes
   - Reference any related issues
   - Request review from maintainers

### Code Standards

- **TypeScript**: Strict mode enabled
- **ESLint**: Follow Next.js/React configurations
- **Prettier**: Consistent code formatting
- **Conventional Commits**: Use standard commit message format

---

## Support

### Contact Information

- **Email**: support@vaulto.ai
- **Address**: 2108 N ST STE N, Sacramento, CA 95816
- **Website**: [vaulto.ai](https://www.vaulto.ai)

### Resources

- **Documentation**: Platform-specific README files in each repository
- **GitHub Issues**: Report bugs and request features
- **Community**: Join our Discord for discussions

### Getting Help

1. **Check Documentation**: Review repository-specific README files
2. **Search Issues**: Look for similar issues on GitHub
3. **Create Issue**: Provide detailed information about your problem
4. **Contact Support**: Reach out via email for urgent matters

---

## License

This project contains proprietary software for Vaulto AI. All rights reserved.

**Important Notice**: Users are responsible for ensuring their trading activities comply with applicable laws and regulations in their jurisdiction. Always conduct your own research and understand the risks before trading RWAs or using DeFi protocols.

---

## Acknowledgments

Built by the Vaulto AI team.

**Special Thanks:**
- Next.js team for the amazing framework
- CoW Protocol for MEV protection
- WalletConnect for multi-wallet support
- CoinGecko for reliable price data
- The open-source community for inspiration and tools

---

<div align="center">

**Vaulto AI** - *Connecting Information, Assets, and Capital*

[Website](https://www.vaulto.ai) • [GitHub](https://github.com/vaulto-ai) • [Support](mailto:support@vaulto.ai)

</div>

