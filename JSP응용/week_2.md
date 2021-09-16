## JSP, MySQL 연동

#### JDBC 드라이버 로딩

> Connection conn = null
> > 연결된 디비를 붙잡고 있는 객체

------------------

> PreparedStatement ps = null
> > 연결된 디비를 겨냥해서 select, insert, delete 같은 sql문을 동작시켜줌
> >
> > ps.executeQuery(); 
> > > 단순히 select만 할 때 사용
> >
> > ps.executeUpdate();
> > > insert, update, delete 같은 테이블에 변화를 가할 때 사용
------------------

> ResultSet rs = null
> > select한 결과를 반환

```
<%
.
.
.

  String url = "{접속할 데이터베이스 시스템, 포트, 디비명}";
  String id = "접속할 아이디";
  String pw = "패스워드";

  Connection conn = null;
  PreparedStatement ps = null;
  ResultSet rs = null;
  String sql = null;
  int hb, year;
  String name, dept, addr;

  try {
  	conn = DriverManager.getConnection(url, id, pw);
  	/* out.println("MysqlDB 서버 연결 성공!<Br>");  */

  	sql = "select * from student";
  	ps = conn.prepareStatement(sql);
  	rs = ps.executeQuery();

  	while (rs.next()) {
  		// rs.getInt("테이블에 있는 필드명");
  		hb = rs.getInt("hakbun");
  		name = rs.getString("name");
  		year = rs.getInt("year");
  		dept = rs.getString("dept");
  		addr = rs.getString("addr");
			
%>
	 학번:<%=hb %> 이름:<%=name %> 학년:<%=year %> 학과:<%=dept %> 주소:<%=addr %> <br>
<%
	  }

	} catch (SQLException sqlerr) {
		out.println("MysqlDB 서버 연결 실패!!<Br>");
		out.println(sqlerr.getMessage() + "<Br>");
	}
%>
```
