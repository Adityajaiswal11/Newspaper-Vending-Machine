#Newspaper Vending Machine (Verilog)

This project implements a Newspaper Vending Machine using Verilog HDL, designed to simulate a simple digital system that accepts coins, verifies the inserted amount, dispenses a newspaper when the correct total is reached, and returns change if overpaid. The design uses a Finite State Machine (FSM) to control operations.

Features
Accepts predefined coin denominations (e.g., ₹1, ₹2, ₹5).
Dispenses a newspaper when the required amount is inserted (e.g., ₹5).
Returns correct change if the inserted amount exceeds the required value.
Rejects invalid input or incomplete payment.
Resettable system to initialize or restart operations.
Designed using behavioral Verilog.
Simulated using a testbench with various transaction scenarios.

📁 Project Structure
bash
Copy
Edit
├── newspaper_vend.v        # Main Verilog module (FSM implementation)
├── newspaper_vend_tb.v     # Testbench for simulation
├── NewsPaperVendingOutput             # (optional) Waveform dump file
├── README.md                # Project documentation
🧠 How It Works
Coin Input: Users insert coins, and the internal counter updates the total amount.

Amount Check: The system compares the accumulated value with the required price of the newspaper.

Dispense Logic:
If the exact amount is inserted, the machine dispenses the newspaper.
If excess amount is inserted, it also returns the change.
Reset: A reset input reinitializes the machine to its idle state.

⚙️ Technologies Used
Verilog HDL for hardware modeling
ModelSim, Vivado, or Riviera-PRO for simulation (user choice)
GTKWave (optional) for waveform viewing

🧪 Test Scenarios
Exact payment: ₹5 → newspaper dispensed
Overpayment: ₹2 + ₹5 → newspaper + ₹2 change
Underpayment: ₹1 + ₹2 → no newspaper
Invalid coins: ignored or error message (depending on implementation)

🚀 Getting Started
Clone the repository.
Open your Verilog simulator of choice.
Compile both the module and the testbench.
Run the simulation and inspect waveform or console outputs.
