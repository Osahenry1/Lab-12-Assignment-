The following program splitTime.c is used to split a time in seconds into the equivalent time
in hours (0-23), minutes (0-59), and seconds (0-59), respectively. But it is incomplete. Please
complete the program.
Sample output:
Enterseconds:2345
Converted format 0 hour 39 mins 5 secs
Enter seconds:3601
Converted format 1 hour 0 mins 1 secs

#include<stdio.h>
// Write the declaration of function split_time
int main(){
int n,hr,min,sec;
printf("Enter seconds:");
scanf("%d",&n);
/* Write the statement to call split_time */
printf("Converted format: %d hour %d mins %d secs", /* Write
the corresponding expressions */ );
return 0;
}
void split_time(long total_sec, int *hr, int *min, int
*sec){ /* Write the statements to calculate hr, min and sec
*/

}