#include<iostream>
using namespace std;

void
findwt (int processes[], int n, int bt[], int wt[])
{
  wt[0] = 0;
  for (int i = 1; i < n; i++)
	{
	  wt[i] = bt[i - 1] + wt[i - 1];
	}
}

void
findtat (int processes[], int n, int bt[], int wt[], int tat[])
{
  for (int i = 0; i < n; i++)
	{
	  tat[i] = bt[i] + wt[i];
	}
}

void
findavgtime (int processes[], int n, int bt[])
{
  int wt[n], tat[n], total_wt = 0, total_tat = 0;

  findwt (processes, n, bt, wt);
  findtat (processes, n, bt, wt, tat);

  cout << "processes " << "brust time " << "WAT " << "TAT";

  for (int i = 0; i < n; i++)
	{
	  total_wt = total_wt + wt[i];
	  total_tat = total_tat + tat[i];
	  cout << "\t\t" << i +1 << "\t  " << bt[i] << "\t  " << wt[i] << "\t  " << tat[i];
	
  cout << "\nAverage waiting time " << (float) total_wt / (float) n;
  cout << "\nAverage turn around time " << (float) total_tat / (float) n;
}
}
int main ()
{
  int processes[] = { 1, 2, 3, 4 };
  int n = sizeof processes / sizeof processes[0];

  int brust_time[] = { 21, 3, 6, 2 };

  findavgtime (processes, n, brust_time);
  return 0;
}
