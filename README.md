# responsive-tailwind-menu-in-React


### Responsive navbar 
	
```js

demo code

```
</details>

### Responsive navbar 
	
```js

import React, { useState } from 'react';
import { Link, useNavigate } from 'react-router-dom';


const Header = () => {
    const [isActive, setIsActive] = useState(false);

    const handleHumbagerMenu = event => {
        setIsActive(current => !current);
    }


    return (
        <div className="header">
            <div className="container mx-auto px-4">
                <nav className="navbar">
                    <Link className="navbar-brand" to="/"><img src={logo} alt="Travel" /></Link>
                    <button className="navbar-toggler" type="button" onClick={handleHumbagerMenu}>
                        <FaBars className='text-[#0f6191] border-[#0f6191]'></FaBars>
                    </button>
                    <div className ={isActive ? 'navbar-collapsed' : 'navbar-collapse'}>
                    <ul className="navbar-nav">
                        <li><Link className="nav-link" to="/">Home</Link></li>
                        <li><Link className="nav-link" to="/tours">Tours</Link></li>
                        <li><Link className="nav-link" to="/faqs">FAQ's</Link></li>
                        {
                            user?.uid ?
                            <>
                            {
                                user?.uid &&
                                <>
                                <li><Link className="nav-link" to="/add-tour">Add Tour</Link></li>
                                <li><Link className="nav-link" to="/reviews">Reviews</Link></li>
                                <li><button className="logout-btn" onClick={handleLogOut}><FiLogOut className="mr-2 text-base"></FiLogOut> Sign Out</button></li>
                                </>
                            }
                            
                            </>
                            :
                            <li><Link className="nav-link" to="/login">Login</Link></li>
                        }
                    </ul>
                  </div>
                </nav>
            </div>
        </div>
    );
};

export default Header;

```
</details>
