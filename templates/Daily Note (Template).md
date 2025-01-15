<% tp.file.include("[[Daily Note Frontmatter (Section Template)]]") %>
## 🤔 Looking Back...

**Three years ago:**

![[<% tp.date.now("YYYY-MM-DD", "P-3Y", tp.file.title, "YYYY-MM-DD") %>#📑 Summary]]

**Two years ago:**

![[<% tp.date.now("YYYY-MM-DD", "P-2Y", tp.file.title, "YYYY-MM-DD") %>#📑 Summary]]

**A year ago:**

![[<% tp.date.now("YYYY-MM-DD", "P-1Y", tp.file.title, "YYYY-MM-DD") %>#📑 Summary]]

**4 weeks ago:**

![[<% tp.date.now("YYYY-MM-DD", "P-4W", tp.file.title, "YYYY-MM-DD") %>#📑 Summary]]

**Last week:**

![[<% tp.date.now("YYYY-MM-DD", "P-1W", tp.file.title, "YYYY-MM-DD") %>#📑 Summary]]

**Yesterday:**

![[<% tp.date.now("YYYY-MM-DD", "P-1D", tp.file.title, "YYYY-MM-DD") %>#📑 Summary]]

<% tp.file.include('[[Journal Summary (Section Template)]]') %>

## 🎯 Objectives

*What am I working towards?*

### 🐉 Personal

- [ ] 
- [ ] 
- [ ] 

### 💼 Work

- [ ] 
- [ ] 
- [ ] 

### 🤝 Connections

- [ ] 

## 🕰️ Timeline

*A representation of the activities for the day.*

### 🗓️ All Day

### ✨ Morning

- **06:00AM to 07:00AM**
    - [ ] 
    - [ ] 
- **07:00AM to 08:00AM**
    - [ ] 
    - [ ] 
- **08:00AM to 09:00AM**
    - [ ] 
    - [ ] 
- **09:00AM to 10:00AM**
    - [ ] 
    - [ ] 
- **10:00AM to 11:00AM**
    - [ ] 
    - [ ] 
- **11:00AM to 12:00PM**
    - [ ] 
    - [ ] 

### 🌤️ Afternoon

- **12:00PM to 01:00PM**
    - [ ] 
    - [ ] 
- **01:00PM to 02:00PM**
    - [ ] 
    - [ ] 
- **02:00PM to 03:00PM**
    - [ ] 
    - [ ] 
- **03:00PM to 04:00PM**
    - [ ] 
    - [ ] 
- **04:00PM to 05:00PM**
    - [ ] 
    - [ ] 
- **05:00PM to 06:00PM**
    - [ ] 
    - [ ] 

### 🌙 Evening
	
- **06:00PM to 07:00PM**
    - [ ] 
- **07:00PM to 08:00PM**
    - [ ] 
- **08:00PM to 09:00PM**
    - [ ] 
    - [ ] 
- **09:00PM to 10:00PM**
    - [ ] 
    - [ ] 

## 📊 Metrics

- 🌦️ Forecast: 16 hrs (6:00AM to 10:00PM)
    - 🐉 Personal: ❓ hrs
    - 💼 Work: ❓ hrs
    - 🤝 Connection:: ❓ hrs
    - 🛡️ Buffer:: ❓ hrs
- 📖 Log: ❓ hrs (❓ to ❓)
    - 🐉 Personal: ❓ hrs
    - 💼 Work: ❓ hrs
    - 🤝 Connection:: ❓ hrs

## 📝 Notes
```dataview
LIST
WHERE file.cday = this.file.day
```