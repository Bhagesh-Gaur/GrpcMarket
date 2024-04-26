
# GrpcMarket: A Cloud-Native gRPC Online Trading Hub

## Overview

GrpcMarket is a distributed online marketplace system, architected to facilitate direct transactions between buyers and sellers through a central platform hosted on Google Cloud VM instances. This system leverages gRPC for communication and Protocol Buffers for efficient data serialization. The marketplace is capable of handling product listings, purchases, real-time notifications, and ratings, ensuring a secure and dynamic e-commerce environment.

## Features

- **Distributed Architecture:** Separate VM instances for buyers, sellers, and the market platform.
- **Real-Time Notifications:** Instant updates on product changes and purchases.
- **Secure Communication:** gRPC and Protocol Buffers ensure secure and efficient data transfer.
- **Scalable Solution:** Easily expandable and manageable for growing numbers of users and listings.

## Tech Stack

- **Google Cloud Platform (GCP):** For creating and managing VM instances.
- **gRPC:** High-performance RPC framework for client-server communication.
- **Protocol Buffers:** Data interchange format used for serializing structured data.
- **Python:** Primary programming language for service logic.
- **Linux:** Preferred operating system for VMs.
- **UUID:** Unique identifier generation for secure transactions.

## Getting Started

Before you begin, ensure you have access to Google Cloud Platform and have Python installed on your local machine.

### Prerequisites

- Google Cloud account with billing set up.
- Basic understanding of VM operations and VPC network configurations in GCP.
- Python 3.6 or higher.

### Installation

1. **Set up VM Instances in GCP:**
   - Create VM instances for the Market, Sellers, and Buyers following the GCP documentation.
   - Update the VPC Firewall rules to allow gRPC traffic.

2. **Environment Setup:**
   - SSH into each VM and clone this repository.
   - Install the required Python packages using pip:

     ```sh
     pip install -r requirements.txt
     ```

3. **Running the Application:**
   - Start the Market server on the central platform VM.
   - Run the Seller and Buyer clients on their respective VMs.

### Configuration

- Configure `ip:port` settings for each VM instance in accordance with your GCP setup.
- Set environment variables for UUID generation as per the provided Python snippet.

## Usage

The platform consists of several RPCs that allow Sellers and Buyers to perform actions such as registering, listing items, purchasing, and rating.

- **Sellers:**
  - Register with the market.
  - Manage product listings.
  - Receive notifications of purchases.

- **Buyers:**
  - Search for products.
  - Buy and rate products.
  - Add items to wishlist for updates.

## Contribution

Contributions to GrpcMarket are welcome! Please adhere to the contribution guidelines provided in the `CONTRIBUTING.md` file.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.
