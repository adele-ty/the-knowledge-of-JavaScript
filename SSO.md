单点登录（Single Sign-On，简称 SSO）是一种用户身份验证和授权的解决方案。在 SSO 系统中，用户只需进行一次登录操作，即可访问多个相关联且互信的应用系统，无需在每个应用中单独登录。这大大提高了用户使用体验，同时也减轻了用户记住多个用户名和密码的负担。  

单点登录背后的核心概念是中央认证服务器（Central Authentication Server）。当用户首次登录时，中央认证服务器会验证用户的身份并颁发一个身份令牌（Token）。随后，用户访问其他关联应用时，应用会识别并验证该令牌。如果令牌有效，应用会授权用户访问资源，而无需用户重新登录。这个过程通常涉及到以下几个步骤：  
1. 用户首次访问某个应用系统时，系统会检查用户是否具有有效的身份令牌。如果没有，应用会将用户重定向至中央认证服务器。  
2. 用户在中央认证服务器上提供其凭据（如用户名和密码）进行登录。  
3. 中央认证服务器验证用户凭据。如果验证成功，服务器会颁发一个身份令牌并将用户重定向回先前访问的应用。  
4. 应用解析并验证身份令牌。如果令牌有效，应用会授权用户访问资源。  
5. 当用户尝试访问其他关联应用时，应用会识别并验证用户的身份令牌。如果令牌有效，应用会授权用户访问资源，而无需重新登录。  

单点登录的优点包括：  
* 提高用户体验：用户只需登录一次，就可以访问多个应用，无需记住多个用户名和密码。  
* 提高安全性：由于用户只需记住一个凭据，因此可以使用更强的密码策略。此外，单点登录简化了用户帐户的管理，例如禁用和启用帐户。  
* 减少开发和维护成本：将身份验证和授权集中管理，可以减少每个应用系统中的重复开发和维护工作。  

单点登录也有一些潜在的缺点，例如：  
* 中心化的风险：单点登录系统可能成为攻击者的主要目标，因为攻破中心认证服务器可能导致对多个应用的访问。  
* 故障点：如果中央认证服务器出现故障，可能会影响所有关联应用的访问。  