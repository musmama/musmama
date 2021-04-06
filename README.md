import sqlite3
con=sqlite3.connect("D:\dersler.db")
cursor=con.cursor()
def tabloyap():
    cursor.execute("CREATE TABLE IF NOT EXISTS ogre(ad TEXT,no INT)")
    con.commit()
def ekle():
    cursor.execute("INSERT INTO ogre VALUES('MUSTAFA',25)")
    con.commit()
    con.close()

tabloyap()
ekle()
