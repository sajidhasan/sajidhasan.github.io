---
layout: post
title: "Basic structure of FIX message"
date: 2024-03-29
category: fix-protocol
permalink: /fix/:title
---

## Introduction to the FIX Protocol

In the fast-paced world of financial trading, efficient and reliable communication is crucial. This is where the Financial Information eXchange (FIX) protocol comes into play. FIX is a standardized protocol that facilitates real-time electronic communication between financial institutions, making trading processes smoother and more efficient. Initially developed in 1992, FIX has become the industry standard for electronic trading, ensuring seamless information exchange across various platforms and systems.

### What is the FIX Protocol?

The FIX protocol is a series of messaging specifications designed to streamline the communication of trade-related information. It covers a broad range of activities, from pre-trade communications and order submissions to post-trade processing. FIX messages are composed of a series of key-value pairs, known as "tags," which convey specific pieces of information.

### Basic Structure of FIX Messages

A FIX message consists of a header, body, and trailer, each containing various tags. Tags are represented as integers, and each tag has a corresponding value that conveys specific information about the trade.

### Key Tags and Their Meanings

Let's explore some of the fundamental tags used in FIX messages and what they represent:

#### 1. **Tag 8: BeginString**

- **Description:** Specifies the beginning of a new FIX message.
- **Example:** `8=FIX.4.2` indicates that the message conforms to the FIX 4.2 version.

#### 2. **Tag 35: MsgType**

- **Description:** Defines the type of FIX message being sent.
- **Example:** `35=D` represents a New Order - Single message, while `35=8` represents an Execution Report.

#### 3. **Tag 49: SenderCompID**

- **Description:** Identifies the sender of the message.
- **Example:** `49=CLIENT1` signifies that the message is sent from the client identified as CLIENT1.

#### 4. **Tag 56: TargetCompID**

- **Description:** Identifies the intended recipient of the message.
- **Example:** `56=BROKER1` indicates that the message is intended for the broker identified as BROKER1.

#### 5. **Tag 34: MsgSeqNum**

- **Description:** Indicates the sequence number of the message.
- **Example:** `34=2` shows that this is the second message in a sequence.

#### 6. **Tag 52: SendingTime**

- **Description:** Specifies the time the message was sent.
- **Example:** `52=20230713-14:30:00` represents a timestamp in the format YYYYMMDD-HH:MM:SS.

#### 7. **Tag 55: Symbol**

- **Description:** Identifies the security being traded.
- **Example:** `55=AAPL` indicates that the security in question is Apple Inc.

#### 8. **Tag 54: Side**

- **Description:** Indicates the side of the order (buy or sell).
- **Example:** `54=1` signifies a buy order, while `54=2` represents a sell order.

#### 9. **Tag 38: OrderQty**

- **Description:** Specifies the quantity of the order.
- **Example:** `38=100` means the order quantity is 100 shares.

#### 10. **Tag 44: Price**

- **Description:** Indicates the price of the order.
- **Example:** `44=150.50` specifies that the price of the order is $150.50.

#### 11. **Tag 10: CheckSum**

- **Description:** Ensures the integrity of the message.
- **Example:** `10=123` is a checksum value used to verify the message's correctness.

### Putting It All Together

Here’s a simple example of a FIX message for a new order:

```
8=FIX.4.2|35=D|49=CLIENT1|56=BROKER1|34=2|52=20230713-14:30:00|55=AAPL|54=1|38=100|44=150.50|10=123|
```

This message can be broken down as follows:

- **8=FIX.4.2:** Indicates the FIX version.
- **35=D:** Specifies that this is a New Order - Single message.
- **49=CLIENT1:** Identifies the sender as CLIENT1.
- **56=BROKER1:** Identifies the recipient as BROKER1.
- **34=2:** Indicates this is the second message in sequence.
- **52=20230713-14:30:00:** Timestamp of when the message was sent.
- **55=AAPL:** The security being traded is Apple Inc.
- **54=1:** The order is a buy order.
- **38=100:** The quantity of the order is 100 shares.
- **44=150.50:** The price of the order is $150.50.
- **10=123:** Checksum value to verify the message's integrity.

### Conclusion

The FIX protocol is a cornerstone of modern electronic trading, enabling efficient and reliable communication between financial institutions. Understanding the basic tags and their meanings is essential for anyone involved in the trading industry. By mastering these key elements, you can ensure smooth and accurate information exchange, ultimately enhancing trading operations.
