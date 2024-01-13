/// An asynchronous function that completes quickly.
async fn quick_task() -> Result<&'static str> {
    println!("START quick_task");
    await!(delay(10)).context("delay failed")?;
    println!("END quick_task");
    Ok("quick_task result")
}

/// An asynchronous function that completes very slowly.
async fn slow_task() -> Result<&'static str> {
    println!("START slow_task");
    await!(delay(10_000)).context("delay failed")?;
    println!("END slow_task");
    Ok("slow_task result" 
    //banner(slowed)-(22)
    
