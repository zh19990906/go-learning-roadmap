# Authentication 与 JWT

认证流程：注册 → 密码哈希 → 登录校验 → 签发 token → middleware 验证。

JWT 常包含 subject、过期时间等 claims。

注意：
- 密码必须使用安全密码哈希，不能明文或普通 hash。
- JWT 不是“加密后的密码”。
- 明确 access token 过期策略。