### **Question:**  
Which two statements are true about **UNDO and REDO**? (Choose two.)

**A.** The generation of **UNDO** generates **REDO**  
**B.** **DML** modifies Oracle database objects and only generates **UNDO**  
**C.** The generation of **REDO** generates **UNDO**  
**D.** **DML** modifies Oracle database objects and only generates **REDO**  
**E.** **DML** modifies Oracle database objects and generates **UNDO** and **REDO**  

---

### **Correct Answers:**  
✅ **A. The generation of UNDO generates REDO**  
✅ **E. DML modifies Oracle database objects and generates UNDO and REDO**  

---

### **Explanation:**

#### **1️⃣ UNDO and REDO in Oracle Database**
- **UNDO**: Used to store old values of data before a change is committed. It helps with **transaction rollback and read consistency**.  
- **REDO**: Used to store information about changes made to the database. It helps **recover transactions in case of failure**.  

---

#### **2️⃣ Why "A" is Correct?**
✅ **A. The generation of UNDO generates REDO**  
- When a **DML operation (INSERT, UPDATE, DELETE)** occurs, Oracle first writes **undo data** (to roll back if needed).  
- Since UNDO is stored in the database, changes to the UNDO segment must also be **logged in the REDO logs** for recovery purposes.  
- **Thus, generating UNDO also generates REDO**.  

📌 **Oracle Reference:**  
➡️ [Managing Undo](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/managing-undo.html)  
➡️ [Introduction to the Redo Log](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/managing-the-redo-log.html)  

---

#### **3️⃣ Why "E" is Correct?**
✅ **E. DML modifies Oracle database objects and generates UNDO and REDO**  
- A **DML statement (INSERT, UPDATE, DELETE)** modifies database objects and must:
  - Generate **UNDO** to allow rollback.
  - Generate **REDO** to ensure changes are recorded for recovery.  
- Oracle writes both **UNDO and REDO records** to maintain data integrity and support transaction management.  

📌 **Oracle Reference:**  
➡️ [Oracle Database Concepts - Undo and Redo](https://docs.oracle.com/en/database/oracle/oracle-database/19/cncpt/database-transaction-units-of-work.html#GUID-B528E1D3-4EDC-49AD-BC69-7C0C370597B6)  

---

### **Why the Other Options Are Incorrect?**

| Option | Explanation |
|--------|------------|
| **B. DML modifies Oracle database objects and only generates UNDO** | ❌ **Wrong** → DML always generates both **UNDO and REDO**. UNDO alone is not enough for crash recovery. |
| **C. The generation of REDO generates UNDO** | ❌ **Wrong** → REDO is generated **because of changes to the database**, not the other way around. UNDO is generated for rollback, not as a result of REDO. |
| **D. DML modifies Oracle database objects and only generates REDO** | ❌ **Wrong** → DML **also generates UNDO**, which allows rollback and read consistency. |

---

### **Final Answer:**  
✅ **A. The generation of UNDO generates REDO**  
✅ **E. DML modifies Oracle database objects and generates UNDO and REDO**  

📚 **Oracle Documentation References:**  
- 🔹 [Managing Undo](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/managing-undo.html)  
- 🔹 [Managing the Redo Log](https://docs.oracle.com/en/database/oracle/oracle-database/19/admin/managing-the-redo-log.html)  
- 🔹 [Oracle Database Concepts - Undo and Redo](https://docs.oracle.com/en/database/oracle/oracle-database/19/cncpt/database-transaction-units-of-work.html#GUID-B528E1D3-4EDC-49AD-BC69-7C0C370597B6)  

---

💡 **Now you’re ready for the next question!** 🚀
