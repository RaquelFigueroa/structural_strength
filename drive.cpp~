//Name:

#include <iostream>
#include <fstream>
#include <iomanip>
#include <cstdlib>//exit()
#include <cmath>
#include <vector>

using namespace std;

//******************************************************
double variance(vector<int> &v);
//
//******************************************************

double standardDev(vector<int> &v);

int main()
{
    ifstream finSteel;
    ifstream finGraph;
    vector<int> vSteel;
    vector<int> vGraph;
    int val;
    
    
    finSteel.open("data1.txt");
    if (finSteel.fail())
    {
        cout << "Data 1 file failed to open." << endl;
        exit(1);
    }
    
    finGraph.open("data2.txt");
    if (finGraph.fail())
    {
        cout << "Data 2 file failed to open." << endl;
        exit(1);
    }
    
    while (finSteel >> val)
    {
        vSteel.push_back(val);
    }
    
   while (finGraph >> val)
    {
        vGraph.push_back(val);
    }
   
    cout << "Steel variance: " << variance(vSteel) << endl;
    cout << "Graphite variance: " << variance(vGraph) << endl;
    
    cout << "Steel standard dev: " << standardDev(vSteel) << endl;
    cout << "Graphite standard dev: " << standardDev(vGraph) << endl;

    finSteel.close();
    finGraph.close();
    return 0;
}
//*****************************************************
double variance(vector<int> &v)
{
    double result(0);
    double mean(0), sum(0), vSum(0);
    for (int i = 0; i < v.size(); i++)
    {
        sum += v[i];
    }
    mean = sum / v.size();
    
    for (int i = 0; i < v.size(); i++)
    {
        vSum += pow( fabs(v[i] - mean), 2);
    }
    
    result = vSum / v.size();
    return result;
}
//End variance function
//********************************************************
//
double standardDev(vector<int> &v)
{
    double result(0);
    result = sqrt(variance(v));
    return result;
}//End standardDev function

