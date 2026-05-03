#include <vector>
#include <algorithm>
#include <queue>
using namespace std;

int minMeetingRooms(vector<vector<int>>& intervals) {
    if (intervals.empty()) return 0;

    // sort by start time
    sort(intervals.begin(), intervals.end());

    // min heap to track end times
    priority_queue<int, vector<int>, greater<int>> pq;

    // first meeting
    pq.push(intervals[0][1]);

    for (int i = 1; i < intervals.size(); i++) {
        // if room is free
        if (intervals[i][0] >= pq.top()) {
            pq.pop();
        }

        // allocate room
        pq.push(intervals[i][1]);
    }

    return pq.size();
}
