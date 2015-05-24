# REST

_在 url 中反映出请求的内容，或者说建立 url 与后端 method 的对应关系_

- level 0：只有一个 url，请求内容都在报文中
- level 1：不同的服务在不同的 url 中，但相关参数在报文中
- level 2：服务与参数都在报文中
- level 3：请求与 level 2 一样，但响应中包括了可能需要访问的 url，用户完全不需要知道服务的结构是怎样的

  例子
  
		{
		  bookmark: {
		    id: 3,
		    uri: "http://bookmark.com/1/dsyer",
		    description: "A description"
		  },
		  links: [
		    {
		      rel: "bookmark-uri",
		      href: "http://bookmark.com/1/dsyer"
		    },
		    {
		      rel: "bookmarks",
		      href: "http://localhost:8080/dsyer/bookmarks"
		    },
		    {
		      rel: "self",
		      href: "http://localhost:8080/dsyer/bookmarks/3"
		    }
		  ]
		}