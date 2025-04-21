# **Neptune GPU Guesser**  

[Neptune GPU Guesser](https://github.com/0xdrpool/neptune_gpu_guesser) is a high-performance **GPU miner** for the [Neptune Crypto](https://neptune.cash) proof-of-work algorithm, optimized for **NVIDIA GPUs** to maximize mining efficiency.  

---

## **📌 GPU Mining Tutorial**  

### **1️⃣ Mining Pool Address**  
```bash
--pool stratum+tcp://neptune.drpool.io:30127
```

### **2️⃣ Latest Miner Releases**  
🔗 **[Download Here](https://github.com/0xdrpool/neptune_gpu_guesser/releases/latest)**  

### **3️⃣ Mining Guide**  

#### **Basic Command**  
```bash
./dr_neptune_prover --pool stratum+tcp://neptune.drpool.io:30127 -w drpoolaccount.xxx
```

---

### **⚙️ Setup on Ubuntu (v18.04+)**  

1. **Get a Mining Address**  
   - Download **[Neptune-Core](https://github.com/Neptune-Crypto/neptune-core/releases/latest)**  
   - Generate a wallet:  
     ```bash
     neptune-cli generate-wallet
     ```

2. **Download the Miner**  
   - Get the latest `ubuntu-dr_neptune_prover-x.x.x.tar.gz` from **[Releases](https://github.com/0xdrpool/neptune_gpu_guesser/releases/latest)**  

3. **Extract & Prepare**  
   ```bash
   tar -zxvf ubuntu-dr_neptune_prover-x.x.x.tar.gz
   cd dr_neptune_prover && chmod +x inner_guesser.sh run_guesser.sh dr_neptune_prover
   ```

4. **Configure Your Account**  
   - Edit `inner_guesser.sh` and update your **drpool account name**.  

5. **Start Mining**  
   ```bash
   ./run_guesser.sh
   ```

---

### **⚡ Setup on HiveOS**  

<img width="674" alt="image" src="https://github.com/user-attachments/assets/5238e28a-ce16-4767-9a54-81f29178a65c" />
 

1. **Miner Name:** `nptprover`  
2. **Installation URL:**  
   - Latest version (e.g., `https://github.com/0xdrpool/neptune_gpu_guesser/releases/v1.0.0/nptprover-1.0.0.tar.gz`)  
3. **Hash Algorithm:** `--`  
4. **Wallet & Worker Template:**  
   - Format: `%WAL%.%WORKER_NAME%`  
   - ⚠️ **Important:** Use your **drpool account name** as the wallet.  

---

### **🚀 Start Mining Now!**  
For support and updates, visit the **[GitHub Repository](https://github.com/0xdrpool/neptune_gpu_guesser)**.  

