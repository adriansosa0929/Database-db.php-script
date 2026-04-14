def get_db_connection():
    conn = pymysql.connect(host=DB_HOST, user=DB_USER, password=DB_PASS, database=DB_NAME, cursorclass=pymysql.cursors.DictCursor)
    return conn


netsh advfirewall firewall add rule name="Flask5000" protocol=TCP dir=in localport=5000 action=allow
