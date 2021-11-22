#include <stdio.h>


int main()
{
    float x, y, z;
    printf("Enter 3 numbers:\n");
    scanf_s("%f, %f, %f", &x, &y, &z);

    if ((x != y) && (x != z) && (y != z) && (x + y + z < 1))
    {
        if ((x < y) && (x < z))
        {
            x = (y + z) / 2;
        }
        else if ((y < x) && (y < z))
            {
                y = (x + z) / 2.0;
            }
            else if ((z < x) && (z < y))
                {
                    z = (x + y) / 2;
                }


    }

    else if ((x < 0) && (y < 0) && (x < y))
        {
            x = (x + y) / 2;
        }
        else if ((x < 0) && (z < 0) && (x < y))
            {
                x = (x + z) / 2;
            }
            else if ((y < 0) && (z < 0) && (x < y))
                {
                    x = (y + z) / 2;
                }
                else if ((x < 0) && (y < 0) && (y < x))
                    {
                        y = (x + y) / 2;
                    }
                    else if ((x < 0) && (z < 0) && (y < x))
                        {
                            y = (x + z) / 2;
                        }
                        else if ((y < 0) && (z < 0) && (y < x))
                            {
                                y = (y + z) / 2;
                                x = x;
                                z = z;
                            };


            };
    printf("x=%f, y=%f, z=%f", x, y, z);
}
