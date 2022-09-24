# second-and-third-largest-number



function thirdLargest(arr, arr_size)
{
    /* There should be 
    atleast three elements */
    if (arr_size < 3)
    {
        console.log(" Invalid Input ");
        return;
    }
    
    // Find first 
    // largest element
    let first = arr[0];
    for (let i = 0;
             i < arr_size ; i++)
        if (arr[i] > first)
            first = arr[i];
    console.log('first',first);
    // Find second 
    // largest element
    let second = 0;
    for (let i = 0; 
             i < arr_size ; i++)
        if (arr[i] > second && 
            arr[i] < first)
            second = arr[i];
            console.log("The second Largest " + 
            "element is ", second);
    // Find third
    // largest element
    let third = 0;
    for (let i = 0; 
             i < arr_size ; i++)
        if (arr[i] > third && 
            arr[i] < second)
            third = arr[i];
            console.log("The third Largest " + 
            "element is ", third);
         
}
  
// Driver Code
  
    let arr = [12, 13, 1, 
                 10, 34, 16,28];
    let n = arr.length;
    thirdLargest(arr, n);
