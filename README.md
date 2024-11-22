```c
/*
 *                                  z
 *                                  |
 *                                  |        (dst 2,6,5)
 *                                  |       /
 *                                  |      /
 *                                  |     /
 *                                  |    /
 *                                  |   /
 *                           _______|__/_________________ y
 *                          /       | /
 *                         /        |/
 *                        O----------------------------- x
 *               (src 0,0,0)
 */

m_degree.x = normalize(toDegrees(-atan2f(m_delta.x, m_delta.y)) + 180.f);
m_degree.y = toDegrees(atan2f(m_delta.z, hypotf(m_delta.x, m_delta.y)));
```
