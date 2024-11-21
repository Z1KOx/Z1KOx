```c
/*
 *                y
 *                |    (dst 2,6)
 *                |    O
 *                |   /
 *                |  /
 *                | /
 *                |/
 * ---------------O---------------x
 *      (src 0,0) |
 *                |
 *                |
 *                |
 *                |
 *                |
 */

m_degree.x = normalize(toDegrees(-atan2f(m_delta.x, m_delta.y)) + 180.f);
m_degree.y = toDegrees(atan2f(m_delta.z, sqrtf(powf(m_delta.x, 2) + powf(m_delta.y, 2))));
```
