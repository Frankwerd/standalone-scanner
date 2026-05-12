# Standalone Scanner

A high-performance, hardware-agnostic scanning interface designed to bridge the gap between physical warehouse inventory and digital ERP systems. 

## 🚀 Overview
The **Standalone Scanner** acts as the "input layer" for supply chain operations. By leveraging standard HID (Human Interface Device) barcode scanners, this tool converts physical stock movements into real-time data updates within an ERP-lite ecosystem. It is built to prioritize speed, reliability, and low-latency feedback.

## 🛠 Features
*   **Hardware Agnostic:** Works with any USB or Bluetooth barcode/QR scanner that acts as a keyboard input.
*   **Real-time Feedback:** Instant UI/UX triggers for successful or failed scans to ensure warehouse accuracy.
*   **ERP Integration:** Communicates via RESTful APIs to sync stock levels directly with your central inventory database.
*   **Error Handling:** Robust validation logic to prevent duplicate entries or invalid SKU processing.

## 🏗 System Architecture
This scanner is designed as a modular component for a larger **ERP-Lite** system:
1.  **Input Layer:** Captures raw input from physical hardware.
2.  **Processing Layer:** Validates the string against the local/remote database schema.
3.  **Sync Layer:** Executes API calls to the ERP backend to update stock counts, adjust order status, or trigger procurement workflows.

## 💻 Technical Stack
*   **Frontend:** React / JavaScript
*   **Communication:** RESTful API Integration
*   **State Management:** Local/Session state for immediate validation

## ⚙️ Getting Started

### Prerequisites
- Node.js (v18.x or higher)
- A barcode scanner (configured to send a "CR" or "Enter" suffix after scanning)

### Installation
```bash
# Clone the repository
git clone https://github.com/Frankwerd/standalone-scanner.git

# Install dependencies
npm install

# Run the development server
npm run dev
