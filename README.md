#include <iostream>
#include <cstdlib>
#include <cstdio>


int main()
{
    setlocale(LC_ALL, "");

    int n;
    double m[n];
    double min;
    double max;
    char end;

    begining:

    std::cout << "Введите кол-во элементов массива\n";
    std::cin >> n;

    std::cout << "Введите массив\n";

    for(int i=0; i<n; ++i)
        std::cin >> m[i];

    min = m[0];
    max = m[0];

    for(int i=1; i<n; ++i)
        {
            if(min >= m[i])
                min = m[i];
            if(max <= m[i])
                min = m[i];
        }

    std::cout << "Максимальным(минимальным) значением массива является: " << min << "(" << max << ")\n" << "Хотите ли продолжить? Y/N\n";
    std::cin >> end;

    if(end == 'Y' || end == 'y')
        goto begining;

    system("PAUSE");
    return 0;

}
