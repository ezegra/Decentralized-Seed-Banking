# Decentralized Seed Banking Smart Contract

## Overview

The Decentralized Seed Banking smart contract is a blockchain-based solution for preserving agricultural biodiversity through community participation. Built on the Stacks blockchain using Clarity, this contract enables farmers, researchers, and conservationists to collaboratively maintain a global seed repository.

## Features

### Core Functionality
- **Seed Deposits**: Users can deposit seeds with detailed metadata including variety, origin, and genetic information
- **Seed Requests**: Community members can request seeds for agricultural or research purposes
- **Verification System**: Multi-layered verification through contract owner and community voting
- **Rating System**: Quality assessment system for deposited seeds
- **Exchange Tracking**: Complete audit trail of all seed exchanges
- **Reward Mechanism**: STX token rewards for seed deposits and verified contributions

### Community Features
- **Reputation System**: Track user contributions and build community trust
- **Community Fund**: Collective funding for seed preservation initiatives
- **Voting System**: Democratic verification process for seed authenticity
- **User Statistics**: Comprehensive tracking of deposits, requests, and contributions

## Contract Architecture

### Data Structures

#### Seeds Map
Stores comprehensive seed information:
- Name, variety, and origin details
- Depositor identity and preservation date
- Quantity and genetic information
- Verification and active status

#### User Contributions Map
Tracks community participation:
- Seeds deposited and requested
- Reputation score and total contributions
- Performance metrics for trust building

#### Exchange System
Complete transaction history:
- Seed requests and approvals
- Exchange records and status
- Community voting and ratings

## Usage Guide

### For Seed Depositors

```clarity
;; Deposit seeds into the bank
(contract-call? .seed-banking deposit-seeds 
  "Heirloom Tomato" 
  "Cherokee Purple" 
  "North America" 
  u150 
  "Open-pollinated, 80-day maturity")
```

### For Seed Requesters

```clarity
;; Request seeds from the bank
(contract-call? .seed-banking request-seeds 
  u1 
  u25 
  "Research on drought resistance")
```

### For Community Members

```clarity
;; Vote for seed verification
(contract-call? .seed-banking vote-for-seed u1 true)

;; Rate seed quality (1-5 scale)
(contract-call? .seed-banking rate-seed u1 u4)
```

## Reward System

### Deposit Rewards
- Large deposits (≥100 seeds): 1 STX
- Medium deposits (≥50 seeds): 0.5 STX
- Small deposits (<50 seeds): 0.1 STX

### Verification Bonus
- Verified seeds: Additional 2 STX reward
- Reputation points: +10 per deposit
- Community recognition through rating system

## Security Features

### Access Control
- Contract owner privileges for critical functions
- User authentication for all operations
- Multi-signature approval for seed requests

### Data Integrity
- Immutable seed records
- Complete audit trail
- Verification through community consensus

### Error Handling
- Comprehensive error codes and messages
- Input validation for all parameters
- Safe arithmetic operations

## Integration Guide

### Frontend Integration
The contract provides read-only functions for displaying:
- Seed catalog with search and filter capabilities
- User profiles with contribution history
- Exchange marketplace for seed trading
- Community statistics and fund status

### API Endpoints
Key read-only functions:
- `get-seed-info`: Retrieve seed details
- `get-user-stats`: Display user contributions
- `get-seed-rating`: Show community ratings
- `get-total-seeds-preserved`: Global statistics

## Development Setup

### Prerequisites
- Stacks CLI installed
- Clarinet for local testing
- Node.js for frontend integration

### Testing
```bash
clarinet test
clarinet check
```

### Deployment
```bash
stacks deploy seed-banking.clar
```

## Contributing

### Community Participation
- Deposit seeds with accurate information
- Verify seed authenticity through voting
- Rate seed quality based on experience
- Contribute to community fund

### Development
- Submit bug reports and feature requests
- Contribute to documentation
- Propose protocol improvements
- Participate in governance discussions

## License

This project is open-source and available under the MIT License.

## Support

For technical support and community discussions:
- GitHub Issues for bug reports
- Community Discord for general questions
- Documentation wiki for detailed guides

## Future Roadmap

### Version 2.0 Features
- Cross-chain compatibility
- Advanced genetic tracking
- Automated distribution system
- Integration with agricultural databases
- Mobile application support

### Community Goals
- Global seed preservation network
- Research collaboration platform
- Educational resource development
- Policy advocacy for biodiversity

---

**Preserving agricultural biodiversity, one seed at a time.**