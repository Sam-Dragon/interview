# Reverse Proxy
- Mainly useful when proxy is required for server
- It is responsible for navigating to applications based on context on server side 
  **Example**: nginx
 
# Scenario
- When 3rd party applications is responsible for managing users, the token per user needs to validated on server side [client side cannot handle due to security issues]
- Hence token is validated on service side and forwarded to client side

# Advantages
- Load Balancing
- Protection from attacks [DDos Attack]
- Global server load balancing
- Caching 
- SSL encryption 
