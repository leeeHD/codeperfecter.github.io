## spring-source-code
###

RestTemplate相关
	// HTTP请求方法枚举，其中的两个方法的写法非常简介，又非常实用
	public enum HttpMethod {

      GET, HEAD, POST, PUT, PATCH, DELETE, OPTIONS, TRACE;


      private static final Map<String, HttpMethod> mappings = new HashMap<String, HttpMethod>(8);

      static {
          for (HttpMethod httpMethod : values()) {
              mappings.put(httpMethod.name(), httpMethod);
          }
      }


      /**
       * Resolve the given method value to an {@code HttpMethod}.
       * @param method the method value as a String
       * @return the corresponding {@code HttpMethod}, or {@code null} if not found
       * @since 4.2.4
       */
      public static HttpMethod resolve(String method) {
          return (method != null ? mappings.get(method) : null);
      }


      /**
       * Determine whether this {@code HttpMethod} matches the given
       * method value.
       * @param method the method value as a String
       * @return {@code true} if it matches, {@code false} otherwise
       * @since 4.2.4
       */
      public boolean matches(String method) {
          return (this == resolve(method));
      }

  }
Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
