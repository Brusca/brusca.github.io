---
title: "How To: Determine MSSql version of an MDF file"
excerpt_separator: "<!--more-->"
categories:
  - How To
tags:
  - MSSQL
  - Mdf
  - SQL Server
---


### Using Powershell:

```
PS > get-content -Encoding Byte "...\foo.mdf" | select-object -skip 0x12064 -first 2
149
2
PS > 2*256+149
661
```

#### Internal Database Version: 661

### With number 661:

| SQL Server Version | Internal Database Version | Database Compatibility Level |
|---|:---:|---:|
| SQL Server 2017 | 869  | 140 |
| SQL Server 2016 | 852 | 130 |
| SQL Server 2014 | 782 | 120 |
| SQL Server 2012 | 706 | 110  |
| SQL Server 2011 Denali | 684 | 110 |
| SQL Server 2008 R2 | 660/661 | 100 |
| SQL Server 2008 | 655 | 100 |
| SQL Server 2005 SP2+ | 612 | 90 |
| SQL Server 2005 | 611 | 90 |
| SQL Server 2000 | 539 | 80 |
| SQL Server 7.0 | 515 | 70 |
| SQL Server 6.5 | 408 | 65 |
| SQL Server 6.0 | ? | 60 |





References:
<br>[rusanu.com](http://rusanu.com/2011/04/04/how-to-determine-the-database-version-of-an-mdf-file/)
<br>[serverfault.com](https://serverfault.com/questions/255591/is-there-a-way-to-determine-the-version-of-sql-server-that-was-used-to-create-an)
