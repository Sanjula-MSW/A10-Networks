 when HTTP_REQUEST {
    if {[HTTP::host] equals "www.abc.com"} {
        # Log the original Host (Optional)
        log "Original Host: [HTTP::host]"
       
        # Rewrite the Host header to www.xyz.com
        HTTP::header replace "Host" "www.xyz.com"
       
        # Log the new Host (Optional)
        log "Rewritten Host: [HTTP::header Host]"
    }
}