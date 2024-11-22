# Nexverse Bid Adapter

## Overview
The Nexverse Bid Adapter enables publishers to connect with the Nexverse Real-Time Bidding (RTB) platform. This adapter supports multiple ad formats, including Banner, Video, and Native ads. By integrating this adapter, publishers can send bid requests to Nexverse’s marketplace and receive high-quality ads in response.

- **Module name**: Nexverse
- **Module type**: Bidder Adapter
- **Supported Media Types**: Banner, Video, Native
- **Maintainer**: anand.kumar@nexverse.ai

## Bidder Parameters
To correctly configure the Nexverse Bid Adapter, the following parameters are required:

| Param Name   | Scope    | Type   | Description                                         |
|--------------|----------|--------|-----------------------------------------------------|
| `uid`        | required | string | Unique User ID assigned by Nexverse for the publisher |
| `pubId`     | required | string | The unique ID for the publisher                     |
| `pubEpid`   | required | string | The unique endpoint ID for the publisher            |
| `placementId`   | required | string | The unique placement ID for the publisher            |
| `placementName`   | required | string | The unique placment Name for the publisher            |

### Example Configuration
The following is an example configuration for a Nexverse bid request using Prebid.js:

```javascript
var adUnits = [{
  code: 'div-gpt-ad-1460505748561-0',
  mediaTypes: {
    banner: {
      sizes: [[300, 250], [300, 600]]
    }
  },
  bids: [{
    bidder: 'nexverse',
    params: {
      uid: '12345',
      pubId: '54321',
      pubEpid: 'abcde',
      placementId: '12345',
      placementName: 'IN_abc.com_mid_300x250'
    },
    isDebug: false // optional i.e need true for testing
  }]
}];
```
