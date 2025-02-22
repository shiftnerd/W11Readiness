# System Compatibility Checker (PowerShell)

This PowerShell script checks your systems for compatibility with Windows 11, such as TPM, Secure Boot, and minimum hardware specifications.

## 🔍 Features

- **Architecture Check**: Ensures the system is x64-based.
- **Screen Resolution Check**: Verifies a minimum vertical resolution of 720 pixels.
- **Processor Check**: Confirms a minimum of 2 cores and 1 GHz clock speed.
- **TPM (Trusted Platform Module) Check**: Detects TPM 2.0 support.
- **Secure Boot Check**: Confirms if Secure Boot is enabled.
- **Memory Check**: Verifies at least 4GB of RAM is available.
- **Disk Space Check**: Ensures at least 64GB of free disk space.

## 2.	Run the Script:
Open PowerShell with administrative privileges and execute:
.\Get-SystemCompatibilityChecks.ps1

##	3.	View the Results:
To format the output neatly:
$results = Get-SystemCompatibilityChecks
$results | Format-Table -AutoSize

✅ Output Example

The script will return a custom object indicating the status of each check:
ArchCheck   ScreenCheck   ProcessorCheck   TPMCheck   SecureBootCheck   MemoryCheck   DiskCheck
---------   ------------  --------------   --------   ---------------   -----------   ---------
1           1             1                1          1                 1             1

Each check will return:
	•	1 – Pass
	•	0 – Fail

⚠️ Prerequisites
	•	PowerShell 5.1 or higher
	•	Administrative privileges for Secure Boot and TPM checks

📄 License

This project is licensed under the MIT License.

🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to submit a pull request or open an issue.

