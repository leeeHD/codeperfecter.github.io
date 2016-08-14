## spring-source-code
###

RestTemplate相关
      // HTTP请求方法枚举，其中的两个方法的写法非常简介，又非常实用
      // 数据结构的使用耶相当到位
      public enum HttpMethod {

        GET, HEAD, POST, PUT, PATCH, DELETE, OPTIONS, TRACE;


        private static final Map<String, HttpMethod mappings = new HashMap<String, HttpMethod(8);

        static {
            for (HttpMethod httpMethod : values()) {
                mappings.put(httpMethod.name(), httpMethod);
            }
        }

        public static HttpMethod resolve(String method) {
            return (method != null ? mappings.get(method) : null);
        }

        public boolean matches(String method) {
            return (this == resolve(method));
        }
        }

Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
