מטלה 1 - גרפים (Classes and Namespaces)

המטרה שלכם במטלה הזאת היא ליצור מחלקה שמייצגת גרף ולממש אלגוריתמים על הגרפים (זה הזמן להזכר בקורס אלגוריתמים 1).

במטלה הזאת הייצוג של הגרף שלכם יתבצע בעזרת מטריצת שכנויות - https://he.wikipedia.org/wiki/%D7%9E%D7%98%D7%A8%D7%99%D7%A6%D7%AA_%D7%A9%D7%9B%D7%A0%D7%95%D7%AA.

הגרף יכול להיות גרף מכוון ולא מכוון וגם גרף ממושקל. מטריצת השכנויות חייבת להיות מטריצה ריבועית.

עליכם לכתוב את הקבצים הבאים:

Graph.cpp
Algorithms.cpp

הקובץ Graph.cpp מכיל מחלקה המייצגת גרף המכילה את הפעולות:

    loadGraph - המקבלת מטריצת שכנויות וטוענת אותה לתוך הגרף
    printGraph - שמדפיסה את הייצוג של הגרף
    getsize - מחזירה את גודל הגרף
    getNeighbors(v) - מקבלת איבר ומחזירה את השכנים שלו
    countWeights - מחזיר את הכמות צלעות של הגרף
    getWeight(i,j) - מקבלת שני איברים ומחזירה את משקל הצלע ביניהם
    operator (+/-/* /++/-- />/>=/</<=/==/!=/ +=/-=/*=) - כל האופורטורים שמבצעים על שני גרפים או על גרף ומספר
    operator<< - אופרטור פלט הדפסה של הגרף
    CHECK_FOR_SIZE(const Graph &g1, const Graph &g2) - בודק האם הגרפים ניתנים לחיבור\חיסור\כפל
    


הקובץ Algorithms.cpp מכיל מימושים לאלגוריתמים על גרפים. ביניהם:

    isConnected(g) - האלגוריתם מקבל גרף ומחזיר 1 אם הגרף קשיר (אחרת מחזיר 0).
    shortestPath(g,start,end) - האלגוריתם מקבל גרף, קודקוד התחלה וקודקוד סיום ומחזיר את המסלול הקל ביותר (במקרה שהגרף לא ממושקל - הקצר ביותר) בין שני הקודקודים. במידה ואין מסלול כזה, האלגוריתם יחזיר -1.
    isContainsCycle(g) - האלגוריתם מקבל גרף ומדפיס מעגל כלשהו. אם לא קיים מעגל בגרף, האלגוריתם יחזיר 0.
    isBipartite(g) - האלגוריתם מקבל גרף ומחזיר את החלוקה של הגרף לגרף דו-צדדי. אם אי אפשר לחלק את הגרף, האלגוריתם יחזיר 0.
    negativeCycle(g) - האלגוריתם מקבל גרף ומוצא מעגל שלילי (כלומר מעגל שסכום המשקלים של הצלעות שלילי). אם לא קיים מעגל כזה, האלגוריתם ידפיס שלא קיים מעגל שלילי.
    DFS(v,visited,parent,g) - האלגוריתם מקבל איבר התחלתי , וקטור האם ביקרתי , וקטור מי ההורה שלי , והגרף ומחזיר את האיבר הסופי אליו הגעתי אם לא יחזיר -1
    BFSColor(g, v, color , groupA, groupA) - האלגוריתם מקבל גרף, איבר התחלתי , וקטור צבעים , וקטור קבוצה1 , וקטור קבוצה2 ומחזיר 1 אם הגרף מתחלק לדו-צדדי (אחרת מחזיר 0)
    constructCyclePath(v,parent) - האלגוריתם מקבל איבר התחלתי ווקטור מי ההורה שלי ומחזיר סטרינג של מעגל אם לא קיים מחזיר סטרינג ריק

הקובץ Demo.cpp ן- MyTest.cpp מכילים דוגמאות של קלטים ופלטים.
