```
#include <iostream>
#include <sstream>

int main()
{
    for( std::string string; std::getline( std::cin, string ); ) {
        int numbers[ 10 ];
        std::istringstream stream( string );
        bool failure = false;
        for( int i = 0; i < 10; ++i ) {
            if( !( stream >> numbers[ i ] ) ) {
                failure = true;
                break;
            }
        }
        
        if( !failure ) {
            for( int i = 0; i < 10; ++i ) {
                std::cout << numbers[ i ] << " ";
            }
        }
        else {
            std::cout << "An error has occured while reading numbers from line" << std::endl;
        }
    }
}

```
