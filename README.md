# mobile-wallet
CREATE TABLE users (  u_id integer PRIMARY KEY,
  name text NOT NULL,  mobile text NOT NULL,  wallet_id integer NOT NULL,
  when_created timestamp without time zone NOT NULL  -- more stuff :)  ); 
  
  CREATE TABLE transfers (  transfer_id integer PRIMARY KEY,
  u_id integer NOT NULL,  source_wallet_id integer NOT NULL,
  dest_wallet_id integer NOT NULL,  send_amount_currency text NOT NULL, 
send_amount_scalar numeric NOT NULL,  receive_amount_currency text NOT NULL,
  receive_amount_scalar numeric NOT NULL,  kind text NOT NULL, 
dest_mobile text,  dest_merchant_id integer, when_created 
timestamp without time zone NOT NULL  -- more stuff :)  );  

CREATE TABLE agents (  agent_id integer PRIMARY KEY, 
name text,  country text NOT NULL,  region text,  city text,  subcity text, 
when_created timestamp without time zone NOT NULL  -- more stuff :)  );  

CREATE TABLE agent_transactions (  atx_id integer PRIMARY KEY, 
u_id integer NOT NULL,  agent_id integer NOT NULL, 
amount numeric NOT NULL,  fee_amount_scalar numeric NOT NULL, 
when_created timestamp without time zone NOT NULL  -- more stuff :)  );  

CREATE TABLE wallets (  wallet_id integer PRIMARY KEY,  currency text NOT NULL,
  ledger_location text NOT NULL,  when_created timestamp without time zone NOT NULL 
-- more stuff :)  ); 
