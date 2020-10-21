# utl-creating-a-web-server-dashboad-app-using-r-shiny
Creating a web server dashboad app using r shiny  

    StackOverflow: Creating a local web server dashboad app using r shiny                                                          
                                                                                                                                   
    The instuctions below will install a local web server that incorporates R shiny.                                               
                                                                                                                                   
    We will create a dashboad which will pop up via a chrome web page.                                                             
                                                                                                                                   
    Example of web server page                                                                                                     
    https://tinyurl.com/y55pjf2y                                                                                                   
    https://github.com/rogerjdeangelis/utl-creating-a-web-server-dashboad-app-using-r-shiny/blob/main/shiny_web_page.png           
                                                                                                                                   
    github                                                                                                                         
    https://tinyurl.com/y5vew2tn                                                                                                   
    https://github.com/rogerjdeangelis/utl-creating-a-web-server-dashboad-app-using-r-shiny                                        
                                                                                                                                   
    /*                         _                       _                                                                           
      __ _     _ __ ___   __ _| | _____  __      _____| |__                                                                        
     / _` |   | `_ ` _ \ / _` | |/ / _ \ \ \ /\ / / _ \ `_ \                                                                       
    | (_| |_  | | | | | | (_| |   <  __/  \ V  V /  __/ |_) |                                                                      
     \__,_(_) |_| |_| |_|\__,_|_|\_\___|   \_/\_/ \___|_.__/                                                                       
     ___  ___ _ ____   _____ _ __                                                                                                  
    / __|/ _ \ `__\ \ / / _ \ `__|                                                                                                 
    \__ \  __/ |   \ V /  __/ |                                                                                                    
    |___/\___|_|    \_/ \___|_|                                                                                                    
                                                                                                                                   
    */                                                                                                                             
    First you need to install the local web server                                                                                 
                                                                                                                                   
    see                                                                                                                            
    https://tinyurl.com/y44fquwp                                                                                                   
    https://foretodata.com/how-to-make-a-standalone-desktop-application-with-shiny-and-electron-on-windows/                        
                                                                                                                                   
    Before step 4, I created a directory. Every thing you need will be in this folder                                              
                                                                                                                                   
    d:/shiny                                                                                                                       
                                                                                                                                   
    and made it the current working directory                                                                                      
                                                                                                                                   
    cd d:/shiny                                                                                                                    
                                                                                                                                   
    You can stop at step 9.3 unlesss you want to create an executable.                                                             
                                                                                                                                   
    /*        _           _        _ _   ____                                                                                      
    | |__    (_)_ __  ___| |_ __ _| | | |  _ \                                                                                     
    | `_ \   | | `_ \/ __| __/ _` | | | | |_) |                                                                                    
    | |_) |  | | | | \__ \ || (_| | | | |  _ <                                                                                     
    |_.__(_) |_|_| |_|___/\__\__,_|_|_| |_| \_\                                                                                    
                                                                                                                                   
                      _                                                                                                            
     _ __   __ _  ___| | ____ _  __ _  ___  ___                                                                                    
    | `_ \ / _` |/ __| |/ / _` |/ _` |/ _ \/ __|                                                                                   
    | |_) | (_| | (__|   < (_| | (_| |  __/\__ \                                                                                   
    | .__/ \__,_|\___|_|\_\__,_|\__, |\___||___/                                                                                   
    |_|                         |___/                                                                                              
    */                                                                                                                             
                                                                                                                                   
    Change directory to                                                                                                            
                                                                                                                                   
    d:\shiny\electron-quick-start\R-Portable-Win\bin                                                                               
                                                                                                                                   
    enter r.exe                                                                                                                    
                                                                                                                                   
    This brings up R command line interface                                                                                        
                                                                                                                                   
    Install these packages                                                                                                         
                                                                                                                                   
    install.packages("shiny")                                                                                                      
    install.packages("shinydashboard")                                                                                             
                                                                                                                                   
    /*                                 _                                                                                           
      ___      _____  _____  ___ _   _| |_ ___                                                                                     
     / __|    / _ \ \/ / _ \/ __| | | | __/ _ \                                                                                    
    | (__ _  |  __/>  <  __/ (__| |_| | ||  __/                                                                                    
     \___(_)  \___/_/\_\___|\___|\__,_|\__\___|                                                                                    
                                                                                                                                   
         _           _     _                         _                                                                             
      __| | __ _ ___| |__ | |__   ___   __ _ _ __ __| |                                                                            
     / _` |/ _` / __| `_ \| `_ \ / _ \ / _` | `__/ _` |                                                                            
    | (_| | (_| \__ \ | | | |_) | (_) | (_| | | | (_| |                                                                            
     \__,_|\__,_|___/_| |_|_.__/ \___/ \__,_|_|  \__,_|                                                                            
                                                                                                                                   
    */                                                                                                                             
    Go to                                                                                                                          
    https://tinyurl.com/y3pntfzn                                                                                                   
    https://stackoverflow.com/questions/64454466/how-to-create-customs-user-interface                                              
                                                                                                                                   
    Dashboard Script by                                                                                                            
    Mriti Agarwal                                                                                                                  
    https://stackoverflow.com/users/14339331/mriti-agarwal                                                                         
                                                                                                                                   
    Copy and paste te code into the R command line                                                                                 
                                                                                                                                   
    library(shiny)                                                                                                                 
    library(shinydashboard)                                                                                                        
                                                                                                                                   
    ui <- dashboardPage(                                                                                                           
      dashboardHeader(),                                                                                                           
      dashboardSidebar(),                                                                                                          
      dashboardBody(                                                                                                               
      box(title="TITLE",status="primary",solidHeader=TRUE,style="",                                                                
          width=2,                                                                                                                 
          h1(strong("$89,90")),                                                                                                    
          h5("Some text here"),                                                                                                    
          hr(),                                                                                                                    
          h4("More text"),                                                                                                         
          hr(),                                                                                                                    
          h4("More text"),                                                                                                         
          hr(),                                                                                                                    
          h4("More text"),                                                                                                         
          hr(),                                                                                                                    
          h4("More text"),                                                                                                         
          hr(),                                                                                                                    
          actionButton("button","Login and subscribe",class="btn-primary")                                                         
      ))                                                                                                                           
                                                                                                                                   
                                                                                                                                   
    )                                                                                                                              
                                                                                                                                   
    server <- function(input, output, session) {                                                                                   
                                                                                                                                   
      observeEvent(input$button, {                                                                                                 
        ## do something                                                                                                            
      })                                                                                                                           
    }                                                                                                                              
                                                                                                                                   
    shinyApp(ui, server)                                                                                                           
                                                                                                                                   
    Hit enter                                                                                                                      
                                                                                                                                   
    /*   _                 _               _                                                                                       
      __| |     ___  _   _| |_ _ __  _   _| |_                                                                                     
     / _` |    / _ \| | | | __| `_ \| | | | __|                                                                                    
    | (_| |_  | (_) | |_| | |_| |_) | |_| | |_                                                                                     
     \__,_(_)  \___/ \__,_|\__| .__/ \__,_|\__|                                                                                    
                              |_|                                                                                                  
    */                                                                                                                             
    You should see the following in chrome                                                                                         
                                                                                                                                   
       _____________________________________________                                                                               
      |                                             |                                                                              
      |  TITLE                                      |                                                                              
      |_____________________________________________|                                                                              
      |                                             |                                                                              
      |    _   ___  ___   ___   ___                 |                                                                              
      |   | | ( _ )/ _ \ / _ \ / _ \                |                                                                              
      |  / __)/ _ \ (_) | (_) | | | |               |                                                                              
      |  \__ \ (_) \__, |\__, | |_| |               |                                                                              
      |  (   /\___/  /_(_) /_/ \___/                |                                                                              
      |   |_|                                       |                                                                              
      |                                             |                                                                              
      |  Some Text Here                             |                                                                              
      |_____________________________________________|                                                                              
      |                                             |                                                                              
      |  More text                                  |                                                                              
      |_____________________________________________|                                                                              
      |                                             |                                                                              
      |  More Text                                  |                                                                              
      |_____________________________________________|                                                                              
      |                                             |                                                                              
      |  More Text                                  |                                                                              
      |_____________________________________________|                                                                              
      |                                             |                                                                              
      |                                             |                                                                              
      |_____________________________________________|                                                                              
      |   _________________________                 |                                                                              
      |  |                         |                |                                                                              
      |  |Login and subscrbe       |                |                                                                              
      |  |_________________________|                |                                                                              
      |_____________________________________________|                                                                              
                                                                                                                                   
                                                                                                                                   
                                                                                                                                   

