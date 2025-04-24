# **Neptune GPU Guesser**  

[Neptune GPU Guesser](https://github.com/0xdrpool/neptune_gpu_guesser) is a high-performance **GPU miner** for the [Neptune Crypto](https://neptune.cash) proof-of-work algorithm, optimized for **NVIDIA GPUs** to maximize mining efficiency.  

---

## **📌 GPU Mining Tutorial**  

### **1️⃣ Mining Pool Address**  
```bash
--pool stratum+tcp://neptune.drpool.io:30127
```

### **2️⃣ Latest Miner Releases**  
🔗 **[Download Here](https://github.com/0xdrpool/neptune_gpu_guesser/blob/main/download.md)**  

### **3️⃣ Mining Guide**  

#### **Basic Command**  
```bash
./dr_neptune_prover --pool stratum+tcp://neptune.drpool.io:30127 -w drpoolaccount.xxx
```

### **4️⃣ Register a DRPool Account​**  

[drpool register](https://drpool.io/user/register)

---

### **⚙️ Setup on Ubuntu (v18.04+)**  

1. **Get a Mining Address**  
   - Download **[Neptune-Core](https://github.com/Neptune-Crypto/neptune-core/releases/latest)**  
   - Generate a wallet:  
     ```bash
     neptune-cli generate-wallet
     ```

2. **Download the Miner**  
   - Get the latest `ubuntu-dr_neptune_prover-x.x.x.tar.gz` from **[Download](https://github.com/0xdrpool/neptune_gpu_guesser/blob/main/download.md)**  (ubuntu: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/ubuntu-dr_neptune_prover-1.0.1.tar.gz)

3. **Extract & Prepare**  
   ```bash
   tar -zxvf ubuntu-dr_neptune_prover-x.x.x.tar.gz
   cd dr_neptune_prover && chmod +x inner_guesser.sh run_guesser.sh stop_guesser.sh dr_neptune_prover
   ```

4. **Configure Your Account**  
   - Edit `inner_guesser.sh` and update your **[drpool](https://drpool.io) account name**.  

5. **Start Mining**  
   ```bash
   ./run_guesser.sh
   ```
6. **View Mining Logs:**
   ![image](https://github.com/user-attachments/assets/920b8afe-5a15-49d4-8fea-8249c09d9d1e)
   ![image](https://github.com/user-attachments/assets/44591ca0-ace7-49bc-a56c-aec35a3ede88)
   - *Received new proposal, start job*: GPU Mining Started
   - *Received new block, waiting for new proposal. stop job*: GPU Mining Paused (Energy Saving Mode)
7. **Stop Mining**
   ```bash
   ./stop_guesser.sh
   ```
---

### **⚡ Setup on HiveOS**  

<img width="674" alt="image" src="https://github.com/user-attachments/assets/5238e28a-ce16-4767-9a54-81f29178a65c" />
 

1. **Miner Name:** `nptprover`  
2. **Installation URL:**  
   - Latest version (e.g., `https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/nptprover-1.0.1.tar.gz`)  
3. **Hash Algorithm:** `--`  
4. **Wallet & Worker Template:**  
   - Format: `%WAL%.%WORKER_NAME%`  
   - ⚠️ **Important:** Use your **[drpool](https://drpool.io) account name** as the wallet.  
5. Real-time Mining Displa
   <img width="1239" alt="image" src="https://github.com/user-attachments/assets/1fc66ae6-5908-4aef-b12a-a5f62b4fac07" />

---

### **🚀 Start Mining Now!**  
For support and updates, visit the **[GitHub Repository](https://github.com/0xdrpool/neptune_gpu_guesser)**.  

