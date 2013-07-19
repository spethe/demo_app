# This file is used by Rack-based servers to start the application.

require ::File.expand_path('../config/environment',  __FILE__)
run Rails.application

case clazz
  when :postgres
    require 'active_record/connection_adapters/postgresql_adapter'
    'ActiveRecord::ConnectionAdapters::PostgreSQLAdapter'.constantize
  when :mysql
    require 'active_record/connection_adapters/abstract_mysql_adapter'
    'ActiveRecord::ConnectionAdapters::AbstractMysqlAdapter'.constantize
  when :sqlite
    require 'active_record/connection_adapters/sqlite3_adapter'
    'ActiveRecord::ConnectionAdapters::SQLite3Adapter'.constantize
  when :oracle
    require 'active_record/connection_adapters/oracle_enhanced_adapter'
    'ActiveRecord::ConnectionAdapters::OracleEnhancedAdapter'.constantize
  else
    clazz
  end

