```cpp
#include <string>
#include <initializer_list>

class User
{
public:
    explicit User( const std::string& name, const std::string& country, const std::initializer_list<std::string>& langs )
        : m_name( name ), m_country( country ), m_langs( langs )
    { }

    ~User() noexcept = default;
    User( const User& ) = delete;
    User( User&& ) = delete;
    User& operator=( const User& ) = delete;
    User& operator=( User&& ) = delete;

private:
    const std::string m_name, m_country;
    const std::initializer_list<std::string> m_langs;
};

int main() {
    const User Z1KO( "Daniel", "Germany", { "C", "C++", "Rust", "Assembly" } );
}
```
