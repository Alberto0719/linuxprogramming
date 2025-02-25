
# UNIX File and Directory Management

Master these commands to efficiently manage your digital workspace.

## 1. Toolbox of Commands

- `ls`: List files/directories
- `cat`: Display or concatenate files
- `rm`: Remove files
- `mv`: Move or rename files
- `mkdir`: Create directories
- `rmdir`: Remove directories
- `file`: Identify file types
- `ln`: Create links
- `tail`: Display file's end
- `head`: Display file's start
- `less` & `more`: Page by page file viewing
- `touch`: Create/update files
- `wc`: Count content in files

## 2. Hands-on Practice

### 2.1 Exploring Files
```bash
cd /etc
ls
ls -la
```

### 2.2 Viewing File Contents
```bash
echo "This is file 1" > file1.txt
echo "This is file 2" > file2.txt
cat file1.txt file2.txt > combined.txt
```

### 2.3 Managing Files
```bash
touch todelete.txt
rm todelete.txt
echo "This is old" > oldname.txt
mv oldname.txt newname.txt
```

### 2.4 Directories Management
```bash
mkdir testDir
mkdir testDir/innerDir
rmdir testDir/innerDir
rmdir testDir
```

### 2.5 Links and File Types
```bash
echo "Original file" > original.txt
ln -s original.txt link.txt
file original.txt
```

### 2.6 File Content
```bash
echo -e "Line 1\nLine 2" > sample.txt
tail -n 1 sample.txt
head -n 1 sample.txt
less sample.txt
more sample.txt
```

### 2.7 File Creation and Update
```bash
touch empty.txt
sleep 60
touch empty.txt
```

### 2.8 Counting Content
```bash
echo -e "Word1 Word2" > count.txt
wc count.txt
```

## 3. Real-world Scenarios

### 3.1 Project Files Organization
```bash
mkdir ProjectDocs Images Code
mv *.txt ProjectDocs/
mv *.jpg Images/
mv *.py Code/
```

### 3.2 System Log Monitoring
```bash
tail -n 20 /var/log/syslog
head /var/log/syslog
ln -s /var/log/syslog ~/syslog_link
```

### 3.3 Weekly Report Generation
```bash
mkdir $(date '+%Y-%m-%d')
mv report.txt $(date '+%Y-%m-%d')/
ln -s $(pwd)/$(date '+%Y-%m-%d')/report.txt ~/report_link.txt
```

## Conclusion
You're now equipped with foundational UNIX commands. Experiment with them and always be cautious, especially with commands like rm.

