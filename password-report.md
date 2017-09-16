---
title: "Analysis of Cracked Passwords"
author: "James Walden"
output: html_document
---



# Password Report

This report describes and visualizes the distributions of the data set of cracked passwords that you provided.  It analyzes passwords by length and also by the character sets used in each passwords.  The four character sets examined are: lower case letters, upper case letters, numbers, and symbols (any non-alphanumeric character).

The table below summarizes the distribution of the passwords, with the Length column describing password lengths, four columns representing each character set and how many passwords include a character from that character set (the TRUE number) and how many passwords do not (the FALSE number), and the Charsets column describing how many passwords contain how many character sets.  The Length column also shows the minimum and maximum password length found in the data set.
<table border=1>
<tr> <th>  </th> <th>     Length </th> <th>   Lower </th> <th>   Upper </th> <th>  Numeric </th> <th> Special </th> <th> Charsets </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> Min.   : 0.00   </td> <td> Mode :logical   </td> <td> Mode :logical   </td> <td> Mode :logical   </td> <td> Mode:logical   </td> <td> 1:   3   </td> </tr>
  <tr> <td align="right"> 2 </td> <td> 1st Qu.:46.00   </td> <td> FALSE:3         </td> <td> FALSE:3         </td> <td> FALSE:3         </td> <td> TRUE:8017      </td> <td> 4:8014   </td> </tr>
  <tr> <td align="right"> 3 </td> <td> Median :47.00   </td> <td> TRUE :8014      </td> <td> TRUE :8014      </td> <td> TRUE :8014      </td> <td> NA's:0         </td> <td>  </td> </tr>
  <tr> <td align="right"> 4 </td> <td> Mean   :47.46   </td> <td> NA's :0         </td> <td> NA's :0         </td> <td> NA's :0         </td> <td>  </td> <td>  </td> </tr>
  <tr> <td align="right"> 5 </td> <td> 3rd Qu.:49.00   </td> <td>  </td> <td>  </td> <td>  </td> <td>  </td> <td>  </td> </tr>
  <tr> <td align="right"> 6 </td> <td> Max.   :60.00   </td> <td>  </td> <td>  </td> <td>  </td> <td>  </td> <td>  </td> </tr>
   </table>

## Password Length

The graph below describes the distribution of password lengths, excluding passwords longer than 20 characters if any were found in the data set.

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3-1.png) 

The following graph is a cumulative density plot of password length, showing the percentage of passwords in the data set that are equal to or shorter than the length specified on the x-axis.  In most data sets, the 50% mark on the y-axis is reached by a length under 10 characters, meaning that 50% of the passwords are no longer than 10 characters.  Does your data set follow this pattern?  

![plot of chunk unnamed-chunk-4](figure/unnamed-chunk-4-1.png) 

## Character Sets

The graph below visualizes how many passwords contain characters from 1, 2, 3, or 4 different character sets.  In most sets of cracked passwords, most passwords only contain one or two character sets.  If one or more of the bars is too small to be seen on the graph, check the table above for the number of passwords using 3 or 4 character sets.

![plot of chunk unnamed-chunk-5](figure/unnamed-chunk-5-1.png) 

The graph below is a [box plot](https://en.wikipedia.org/wiki/Box_plot) that visualizes the length of passwords containing characters from 1, 2, 3, or 4 different character sets.  The box includes the middle 50% of the passwords by length, while the line through the middle of the box is the median length.  The remaining data points are included within the range of the "whiskers" with the exception of outliers, which are points indicating passwords that are far longer than typical.

![plot of chunk unnamed-chunk-6](figure/unnamed-chunk-6-1.png) 
